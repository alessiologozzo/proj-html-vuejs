<template>
    <section>

        <div class="container">

            <div class="row justify-content-center align-items-center">

                <div class="col-12 col-md-6 text-center py-3">
                    <h2>Subscribe Now to Our Newsletter !</h2>
                </div>

                <div class="col-12 col-md-6 d-flex justify-content-center align-items-center py-3">
                    <div class="input-container">
                        <input @keyup.enter="submitInput($event)" type="text" placeholder="Email address...">


                        <div @click="submitInput($event)" class="al-enter">
                            <i class="fa-solid fa-paper-plane"></i>
                        </div>

                    </div>
                </div>

            </div>

        </div>

    </section>
</template>

<script>
    export default {
        name: "AppNewsletter",

        methods: {
            submitInput(e){
                e.target.value = "";
                e.target.placeholder = "Thanks for subscribing!";
            }
        },
    }
</script>

<style lang="scss" scoped>
    @import "../assets/colors.scss";

    section{
        background-color: $app_red;
        padding: 4rem 0;
    }

    h2{
        color: white;
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
</style>