<template>
    <section>
        <div class="container">

            <div class="d-flex flex-column justify-content-center align-items-center">
                <img class="al-events-img mb-4" src="../assets/img/upcoming-events-calendar-icon.png" alt="events">
                <h2 class="al-bg-red mb-5">Upcoming Events</h2>
            </div>

            <div class="row justify-content-center">
                <div v-for="date in coachingDates" class="col-12 col-md-6 col-lg-4">
                    <AppCoaching :date="date" />
                </div>
            </div>

            <div class="d-flex justify-content-center py-4">
                <a class="al-gold-button" href="#">View All Events</a>
            </div>
        </div>
    </section>
</template>

<script>
    import { coachingDates } from '../assets/data.js';
    import AppCoaching from './AppCoaching.vue';

    export default {
        name:"AppEvents",

        components: {
            AppCoaching
        },

        data() {
            return {
                coachingDates: coachingDates
            }
        },
    }
</script>

<style lang="scss" scoped>
    @import "../assets/colors.scss";
    @import "../assets/utilities.scss";

    section{
        background-color: $app_red;
        color: white;
        padding-top: 5rem;
        padding-bottom: 2rem;
    }

    .al-events-img{
        width: 70px;
    }

    .al-gold-button{
        padding: 1.4rem 3.3rem;
        box-shadow: 1px 10px 20px 2px #cc5454;

        &:hover{
            transform: translate(1.06);
        }
    }
</style>