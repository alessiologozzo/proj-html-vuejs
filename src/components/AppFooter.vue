<template>
    <footer>

        <div class="container">

            <div class="row">

                <div class="col-12 col-md-6 col-lg-3 d-flex flex-column justify-content-center align-items-center gap-3 pt-md-3 al-eduprime-m">
                    <img class="al-logo" src="../assets/img/theme_eduprime_logo.png" alt="logo">

                    <p class="text-center text-md-start">EduPrime is the most versatile WordPress theme for educational purposes, showcasing universities, courses, secondary schools etc.</p>
                
                    <div class="d-flex gap-2">
                        <a href="#" class="al-circle"><i class="fa-brands fa-facebook-f"></i></a>
                        <a href="#" class="al-circle"><i class="fa-brands fa-twitter"></i></a>
                        <a href="#" class="al-circle"><i class="fa-brands fa-instagram"></i></a>
                    </div>
                </div>

                <div class="col-12 col-md-6 col-lg-3 col-xl-2 d-flex flex-column justify-content-center align-items-center pt-5 pt-md-0 al-get-m">
                    <h6 class="pb-4">Get EduPrime</h6>

                    <a href="#" v-for="getData in footerDatas.gets" class="al-gold-hover">{{ getData }}</a>
                </div>

                <div class="col-12 col-md-6 col-lg-2 d-flex flex-column justify-content-center align-items-center pt-5 al-networking-m">
                    <h6 class="pb-4">Networking</h6>

                    <a href="#" v-for="networking in footerDatas.networkings" class="al-gold-hover">{{ networking }}</a>
                </div>

                <div class="col-12 col-md-6 col-lg-4 col-xl-5 d-flex flex-column justify-content-center align-items-center pt-5">
                    <div class="input-container">
                        <input @keyup.enter="submitInput($event)" type="text" placeholder="Search...">

                        <div @click="submitInput($event)" class="al-enter">
                            <i class="fa-solid fa-paper-plane"></i>
                        </div>
                    </div>

                    <h6 class="pt-5 pb-3 al-search-translate">Search Categories</h6>

                    <div class="d-flex flex-wrap justify-content-center justify-content-md-end gap-2">
                    
                        <a href="#" v-for="category in footerDatas.categories" class="al-border-button mt-2 text-uppercase">{{ category }}</a>

                    </div>

                    <span class="al-rights pt-4 pb-5">ModelTheme. All Rights reserved.</span>
                </div>

            </div>

        </div>

        <div @click="goTop()" class="al-arrow">
            <i class="fa-solid fa-chevron-up"></i>
        </div>

        <div class="al-theme-container">
            <a href="#" class="al-theme">
                <img class="al-img-1" src="../assets/svg/svg-3.svg" alt="svg3">
                <i>Purchase Theme</i>
            </a>
            <a href="#" class="al-theme">
                <img class="al-img-2" src="../assets/svg/svg-2.svg" alt="svg2">
                <i>Related Themes</i>
            </a>
        </div>
    </footer>
</template>

<script>
    import { footerDatas } from "../assets/data.js";

    export default {
        name: "AppFooter",

        data() {
            return {
                footerDatas: footerDatas
            }
        },
        
        methods: {
            submitInput(e){
                e.target.value = "";
                e.target.placeholder = "Search not available";
            },

            goTop(){
                window.scrollTo(0, 0);
            }
        }
    }
</script>

<style lang="scss" scoped>
    @import "../assets/colors.scss";

    footer{
        background-color: $app_red;
        color: white;
        padding: 7rem 0 9rem;
        position: relative;
    }

    .al-logo{
        width: 200px;
    }

    .al-circle{
        width: 40px;
        height: 40px;
        border: 2px solid $app_gold;
        border-radius: 50%;
        display: flex;
        justify-content: center;
        align-items: center;
        transition: transform 300ms;

        &:hover{
            transform: scale(1.1);
        }
    }

    a{
        color: white;
        text-decoration: none;

        &:hover{
            color: white;
        }
    }

    .al-gold-hover{
        
        &:hover{
            color: $app_gold;
        }
    }

    .input-container{
        width: 95%;
        position: relative;
    }

    input[type="text"]{
        width: 100%;
        padding: 1.6rem 1rem;
        border-radius: 40px;
        background-color: white;
        color: black;
        border: 1px solid white;
    }
    
    ::placeholder{
        color: black;
        opacity: 0.7;
    }

    .al-enter{
        height: 78px;
        width: 78px;
        position: absolute;
        top: 50%;
        right: 0;
        transform: translateY(-50%);
        display: flex;
        justify-content: center;
        align-items: center;
        background-color: $app_gold;
        border-radius: 50%;
        cursor: pointer;
    }

    .al-border-button{
        background-color: $app_red;
        border: 2px solid white;
        padding: 0.5rem 0.7rem;
        border-radius: 30px;
        transition: transform 300ms;

        &:hover{
            transform: scale(1.1);
        }
    }

    .al-rights{
        color: $app_gold;
    }

    .al-arrow{
        position: absolute;
        bottom: 2rem;
        right: 2rem;
        background-color: $app_gold;
        display: flex;
        justify-content: center;
        align-items: center;
        color: white;
        width: 50px;
        height: 50px;
        border-radius: 50%;
        cursor: pointer;
        transition: transform 300ms;

        &:hover{
            transform: scale(1.1);
        }

        i{
            font-size: 1.2rem;
        }
    }

    .al-theme-container{
        position: absolute;
        bottom: 2rem;
        left: 2rem;
        display: flex;
        flex-flow: column nowrap;
        gap: 0.8rem;
    }

    .al-theme{
        background-color: #454545;
        display: flex;
        justify-content: center;
        align-items: center;
        gap: 0.6rem;
        padding: 0.6rem 1.4rem;
        box-shadow: 2px 2px 20px 1px #924141;
        border-radius: 6px;
        color: lightgray;
        transition: transform 300ms;

        &:hover{
            transform: scale(1.05);
        }
    }

    .al-img-1{
        width: 20px;
    }

    .al-img-2{
        width: 25px;
    }

    @media screen and (min-width: 768px){
        .al-networking-m{
            margin-top: 0.2rem;
        }

        .al-search-translate{
            transform: translateX(50%);
        }

        .al-rights{
            transform: translateX(13%);
        }

        .al-logo{
            transform: translateX(-5%);
        }
    }

    @media screen and (min-width: 992px){
        .al-networking-m{
            margin-top: -11.5rem;
        }

        .al-get-m{
            margin-top: -8.3rem;
        }

        .al-eduprime-m{
            margin-top: -5.5rem;
        }

        .al-search-translate{
            transform: translateX(34%);
        }

        .al-rights{
            transform: translateX(6%);
        }
    }

    @media screen and (min-width: 1200px){
        .al-networking-m{
            margin-top: -7.5rem;
        }

        .al-get-m{
            margin-top: -4.5rem;
        }

        .al-eduprime-m{
            margin-top: -3.1rem;
        }

        .al-search-translate{
            transform: translateX(80%);
        }

        .al-rights{
            transform: translateX(38%);
        }

        .al-logo{
            transform: translateX(-7%);
        }
    }

    @media screen and (min-width: 1400px){
        .al-networking-m{
            margin-top: -7rem;
        }

        .al-get-m{
            margin-top: -4rem;
        }

        .al-eduprime-m{
            margin-top: -4rem;
        }

        .al-search-translate{
            transform: translateX(102%);
        }

        .al-rights{
            transform: translateX(50%);
        }

        .al-logo{
            transform: translateX(-12%);
        }
    }
</style>