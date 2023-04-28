<template>
    <section>

        <div class="container">

            <div class="row">

                <div class="col-12 col-lg-6 pt-4 d-flex justify-content-center">

                    <img class="al-w" src="../assets/img/Girl-Illustration.png" alt="examIllustration">

                </div>

                <div class="col-12 col-lg-6 d-flex flex-column align-items-start gap-3 pt-4">
                    <img class="al-exam pb-2" src="../assets/img/Exam-icon-1.png" alt="exam">

                    <h2>Variable fees for international students</h2>

                    <p>EduPrime has gathered teachers from around the globe to brainstorm in order to facilitate the evaluation of our students. Every teacher from our university has an influence on how students are evaluated at his/her subject.</p>
                
                    <a href="#" class="al-red-button">List of Fees</a>
                </div>

            </div>

        </div>

    </section>
</template>

<script>
    export default {
        name: "AppVariable"
    }
</script>

<style lang="scss" scoped>
    @import "../assets/utilities.scss";

    section{
        padding: 4rem 0;
    }

    .al-exam{
        width: 70px;
    }

    .al-red-button{
        padding: 1.2rem 3rem;
    }

    .al-w{
        width: 80%;
    }

    @media screen and (min-width: 992px){
        .al-w{
            width: 100%;
        }
    }
</style>