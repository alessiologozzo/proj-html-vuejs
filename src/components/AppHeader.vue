<template>
    <header>
        <nav class="d-flex justify-content-between align-items-center px-4"> 
            <img src="../assets/img/theme_eduprime_logo.png" alt="logo" class="al-logo">
            <div class="d-none d-xl-flex gap-4">
                <div v-for="link in links" class="d-flex gap-2 align-items-center">
                    <div v-if="!link.arrow">
                        <a href="#" class="al-a-color">{{ link.content }}</a>
                    </div>
                    <div v-else @click.stop="showMenu($event)" class="al-menu-data position-relative d-flex gap-2 justify-content-center align-items-center al-a-color">
                        <a href="#">{{ link.content }}</a>
                        <i class="fa-solid fa-caret-down al-fs-small"></i>
                        <div class="al-menu">
                            <div class="al-menu-item">Something</div>
                            <div class="al-menu-item">Something else</div>
                        </div>
                    </div>
                </div>
                <a href="#" class="al-gold-button text-uppercase">view courses</a>
            </div>
            <div @click="showMenu($event)" class="d-xl-none al-bars al-menu-data position-relative">
                <i class="fa-solid fa-bars"></i>
                <div class="al-menu">
                    <div v-for="link in links" class="al-menu-item">
                        <span>{{ link.content }}</span>
                    </div>
                </div>
            </div>
        </nav>

        <div class="container d-flex flex-column justify-content-center align-items-center gap-3 text-center my-5 pt-3 pb-5">
            <h1>Key to your success</h1>
            <p class="px-0 px-md-5 al-w">EduPrime is the most versatile WordPress theme for educational puroposes, showcasing universities, courses, secondary schools etc.</p>
            <div class="d-flex gap-3 flex-wrap justify-content-center">
                <a href="#" class="al-gold-button d-flex justify-content-center align-items-center gap-2"><i class="fa-solid fa-magnifying-glass"></i><span>Search courses</span></a>
                <a href="#" class="al-white-button d-flex justify-content-center align-items-center gap-2"><i class="fa-solid fa-user-plus"></i><span>Apply for university</span></a>
            </div>
        </div>

        <aside class="d-none d-md-flex">
            <a href="#"><i class="fa-solid fa-cart-shopping"></i></a>
            <a href="#"><i class="fa-regular fa-newspaper"></i></a>
            <a href="#"><i class="fa-solid fa-compass"></i></a>
        </aside>
        <img src="../assets/img/Wave-1.png" alt="wave" class="al-wave">
    </header>
</template>

<script>
    import { navLinks } from "../assets/data.js";
    import { showMenu } from "../assets/menu.js";

    export default {
        name: "AppHeader",
        
        data() {
            return {
                links: navLinks
            }
        },

        methods: {
            showMenu: showMenu
        },
    }
</script>

<style lang="scss" scoped>
    @import "../assets/utilities.scss";
    
    header{
        background: linear-gradient(rgb(229, 103, 104, 0.8), rgb(229, 103, 104, 0.8)), url("../assets/img/theme_slider2_bg-1.jpg");
        background-size: cover;
        color: white;
        overflow-x: hidden;
        padding-top: 1rem;
        position: relative;
    }

    .al-logo{
        height: 3.5rem;
    }

    .al-wave{
        height: 100px;
    }

    .al-a-color{
        color: white;
        text-decoration: none;
        cursor: pointer;
        
        a{
            color: white;
            text-decoration: none;
        }

        &:hover{
            color: $app_gold;

            a{
                color: $app_gold;
            }
        }
    }

    .al-bars{
        font-size: 1.9rem;
        cursor: pointer;
        transition: color 300ms;

        &:hover{
            color: $app_gold;
        }

        .al-menu{
            font-size: 1rem;
        }
    }
    .al-fs-small{
        font-size: 0.7rem;
    }

    aside{
        position: absolute;
        top: 50%;
        left: 0;
        transform: translateY(-50%);
        display: flex;
        flex-flow: column nowrap;
        gap: 0.8rem;
        font-size: 1.4rem;
        background-color: $app_gold;
        padding: 0.9rem 0.9rem;
        border-radius: 0 5px 5px 0;
        box-shadow: 2px 2px 30px 2px #a55053;

        a{
            color: white;
            text-decoration: none;
            transition: transform 300ms;

            &:hover{
                transform: scale(1.2);
            }
        }
    }

    @media screen and (min-width: 992px){
        .al-w{
            width: 650px;
        }
    }

    @media screen and (min-width: 1400px){
        .al-wave{
            width: 100%;
            height: auto;
        }
    }
</style>