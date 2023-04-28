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
            <i @click="showBg1()" class="fa-solid fa-cart-shopping"></i>
            <i @click="showBg2()" class="fa-regular fa-newspaper"></i>
            <i @click="showBg3()" class="fa-solid fa-compass"></i>
        </aside>
        <img src="../assets/img/Wave-1.png" alt="wave" class="al-wave">

        <div id="bg-container-1" class="al-bg-1"></div>
        <div id="bg-container-2" class="al-bg-2 al-opacity"></div>
        <div id="bg-container-3" class="al-bg-3 al-opacity"></div>
    </header>
</template>

<script>
    import { navLinks } from "../assets/data.js";
    import { showMenu } from "../assets/menu.js";

    export default {
        name: "AppHeader",
        
        data() {
            return {
                links: navLinks,
                activeBg: 1,
                interval: null
            }
        },

        methods: {
            showMenu: showMenu,

            showBg1(){
                let container1 = document.getElementById("bg-container-1");
                let container2 = document.getElementById("bg-container-2");
                let container3 = document.getElementById("bg-container-3");
                
                if(container1.classList.contains("al-opacity"))
                    container1.classList.remove("al-opacity");

                if(!container2.classList.contains("al-opacity"))
                    container2.classList.add("al-opacity");

                if(!container3.classList.contains("al-opacity"))
                    container3.classList.add("al-opacity");

                this.activeBg = 1;
                clearTimeout(this.interval);
                this.interval = setTimeout(this.changeBg, 7000);
            },

            showBg2(){
                let container1 = document.getElementById("bg-container-1");
                let container2 = document.getElementById("bg-container-2");
                let container3 = document.getElementById("bg-container-3");
                
                if(!container1.classList.contains("al-opacity"))
                    container1.classList.add("al-opacity");

                if(container2.classList.contains("al-opacity"))
                    container2.classList.remove("al-opacity");

                if(!container3.classList.contains("al-opacity"))
                    container3.classList.add("al-opacity");

                this.activeBg = 2;
                clearTimeout(this.interval);
                this.interval = setTimeout(this.changeBg, 7000);
            },

            showBg3(){
                let container1 = document.getElementById("bg-container-1");
                let container2 = document.getElementById("bg-container-2");
                let container3 = document.getElementById("bg-container-3");
                
                if(!container1.classList.contains("al-opacity"))
                    container1.classList.add("al-opacity");

                if(!container2.classList.contains("al-opacity"))
                    container2.classList.add("al-opacity");

                if(container3.classList.contains("al-opacity"))
                    container3.classList.remove("al-opacity");

                this.activeBg = 3;
                clearTimeout(this.interval);
                this.interval = setTimeout(this.changeBg, 7000);

            },

            changeBg(){
                switch(this.activeBg){
                    case 1:
                        this.showBg2();
                        this.activeBg = 2;
                        break;

                    case 2:
                        this.showBg3();
                        this.activeBg = 3;
                        break;

                    case 3:
                        this.showBg1();
                        this.activeBg = 1;
                        break;
                }
            }
        },

        mounted() {
            this.interval = setTimeout(this.changeBg, 7000);
        },
    }
</script>

<style lang="scss" scoped>
    @import "../assets/utilities.scss";
    
    header{
        background: linear-gradient(rgb(229, 103, 104, 0.8), rgb(229, 103, 104, 0.8));
        background-size: cover;
        color: white;
        overflow-x: hidden;
        padding-top: 1rem;
        position: relative;
    }

    .al-bg-1, .al-bg-2, .al-bg-3{
        position: absolute;
        top: 0;
        bottom: 0;
        left: 0;
        right: 0;
        background-size: cover;
        background-position: center;
        background-repeat: no-repeat;
        z-index: -10;
        transition: opacity 2s;
    }

    .al-bg-1{
        background-image: url("../assets/img/theme_slider2_bg-1.jpg");
    }

    .al-bg-2{
        background-image: url("../assets/img/theme_slider3_bg-1.jpg");
    }

    .al-bg-3{
        background-image: url("../assets/img/theme_slider1_bg-1.jpg");
    }

    .al-opacity{
        opacity: 0;
        transition: opacity 2s;
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
        gap: 1.2rem;
        font-size: 1.4rem;
        background-color: $app_gold;
        padding: 0.9rem 0.9rem;
        border-radius: 0 5px 5px 0;
        box-shadow: 2px 2px 30px 2px #a55053;

        i{
            transition: transform 300ms;
            cursor: pointer;

            &:hover{
                transform: scale(1.15);
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