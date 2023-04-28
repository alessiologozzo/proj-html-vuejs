<template>
    <section>
        <div class="container d-flex flex-column justify-content-center align-items-center">
            <h2 class="text-center">Faculties available at EduPrime</h2>
            <p class="text-center pt-4 pb-5 al-w">A single university with a load of courses, tailored to satisfy any student's needs.</p>
        </div>

        <div class="d-flex justify-content-center al-border-y">
            <div class="container d-flex justify-content-center flex-wrap">
                <div v-for="(facultyData, index) in facultyDatas" class="al-col">
                    <FacultyCard @activeChanged="(i) => activeFaculty = i" :cardData="facultyData" :cardIndex="index" :cardActive="activeFaculty" :class="{'al-active': isActive(index)}"/>
                </div>
            </div>

        </div>

        <div class="container py-4">
            <div class="row justify-content-center">
                <div class="col-12 col-md-6 d-flex justify-content-center pt-3">
                    <img :src="getUrl()" alt="err">
                </div>

                <div class="col-12 col-md-6 pt-5 d-flex flex-column align-items-center align-items-md-start">
                    <h4>{{ facultyDatas[activeFaculty].name }}</h4>
                    <p class="pt-2 pt-md-4 pb-3 al-grey">{{ facultyDatas[activeFaculty].text }}</p>
                    <a href="#" class="d-inline-block al-red-button">Read More</a>
                </div>
            </div>
        </div>

        <div class="al-wave-container"></div>
    </section>
</template>

<script>
    import { facultyDatas } from '../assets/data.js';
    import FacultyCard from './FacultyCard.vue';

    export default {
        name: "AppFaculties",

        components: {
            FacultyCard
        },

        data() {
            return {
                facultyDatas: facultyDatas,
                activeFaculty: 0
            }
        },

        methods: {
            isActive(index){
                let result = false;

                if(this.activeFaculty == index)
                    result = true;

                return result;
            },

            getUrl(){
                return new URL(this.facultyDatas[this.activeFaculty].srcIllustration, import.meta.url).href;
            }
        },
    }
</script>

<style lang="scss" scoped>
    @import "../assets/colors.scss";
    @import "../assets/utilities.scss";

    section{
        padding-top: 2rem;
    }

    .al-col{
        width: 50%;
        border: 1px solid #eaeaea;
    }

    .al-border-y{
        border-top: 1px solid #eaeaea;
        border-bottom: 1px solid #eaeaea;
        box-shadow: 1px 0 30px 2px #eaeaea;
    }

    .al-active{
        background-color: $app_red;
        color: white;
    }

    img{
        width: 80%;
    }

    .al-wave-container{
        width: 100%;
        min-height: 200px;
        background-image: url("../assets/svg/svg-0.svg");
        background-position: left bottom;
        background-size: cover;
    }

    .al-grey{
        color: #686868;
    }

    .al-red-button{
        &:hover{
            transform: scale(1.07);
        }
    }

    @media screen and (min-width: 576px){
        .al-col{
            width: calc(100% / 3);
        }
    }

    @media screen and (min-width: 768px){
        img{
            width: 100%;
        }

        .al-w{
            width: 400px;
        }
    }

    @media screen and (min-width: 992px){
        .al-col{
            width: calc(100% / 5);
        }

        img{
            width: 80%;
        }
    }

    @media screen and (min-width: 1200px){

        img{
            width: 70%;
        }
    }
</style>