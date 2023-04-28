<template>
    <section>
        <div class="al-wave-container"></div>
        <div class="container">
            <h2 class="pb-4 text-center text-md-start">Latest Courses</h2>

            <div class="row align-items-stretch">

                <div v-for="latestData in latestDatas" class="col-12 col-md-6 col-lg-3 px-5 px-md-2">
                    <AppLesson :lessonData="latestData" />
                </div>

            </div>
        </div>
    </section>
</template>

<script>
    import { latestDatas } from '../assets/data.js';
    import AppLesson from "./AppLesson.vue"

    export default {
        name: "AppLatest",

        data() {
            return {
                latestDatas: latestDatas
            }
        },

        components: {
            AppLesson
        }
    }
</script>

<style lang="scss" scoped>
    section{
        margin-top: -0.5rem;
        padding-bottom: 5rem;
    }
    .al-wave-container{
        width: 100%;
        min-height: 200px;
        background-image: url("../assets/svg/svg-1.svg");
        background-position: left top;
        background-size: cover;
    }
</style>