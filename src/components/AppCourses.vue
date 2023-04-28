<template>
    <section class="al-home-bg position-relative">
            <div class="container">
                <div class="row">
                    <div class="col-12 col-lg-6 d-flex flex-column gap-3 align-items-start pt-3">
                        <img class="al-book pb-2" src="../assets/img/Books-icon.png" alt="books">
                        <h2>Thousands of courses for any type of student</h2>
                        <p>At EduPrime, it doesn't matter what domain you wish to pursue a career in. Here you can find a course that satisfies your needs within a click away and applies for a course in a matter of minutes. EduPrime is ranked as the most versatile university in the world, thanks to the numbers of courses it provides.</p>
                        <a href="#" class="al-gold-button">Browse through courses</a>
                    </div>

                    <div class="col-12 col-lg-6 pt-5 pt-lg-3 d-flex justify-content-center align-items-center">
                        <img class="al-w-85 al-w-lg-100" src="../assets/img/Graduation-Illustration.png" alt="graduation">
                    </div>
                </div>
            </div>

            <div class="al-bubble-speech">
                <i>Purchase EduPrime on Envato Market</i>
                <div class="al-clip"></div>
            </div>
        </section>
</template>

<script>
    export default {
        name: "AppCourses"
    }
</script>

<style lang="scss" scoped>
    @import "../assets/utilities.scss";

    .al-book{
        width: 70px;
    }

    .al-home-bg{
        background-image: url("../assets/img/home-background.png");
        background-size: contain;
        background-repeat: no-repeat;
        background-position: right;
    }

    .al-w-85{
        width: 85%;
    }

    .al-bubble-speech{
        position: absolute;
        top: 0;
        left: 2rem;
        padding: 0.3rem 0.8rem;
        border-radius: 6px;
        background-color: #1a1a1a;
        color: white;
        font-size: 0.9rem;
        max-width: 16rem;
        text-align: center;
    }

    .al-clip{
        width: 10px;
        height: 20px;
        background-color: #1a1a1a;
        clip-path: polygon(50% 0, 100% 50%, 50% 100%, 0 50%);
        position: absolute;
        bottom: -10px;
        left: 50%;
        transform: translateX(-50%);
    }

    .container{
        padding: 7rem 1.5rem;
    }

    @media screen and (min-width: 992px){
        .al-w-lg-100{
            width: 100%;
        }
    }
</style>