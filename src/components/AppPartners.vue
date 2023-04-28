<template>
    <section>

        <div class="container text-center d-flex flex-column justify-content-center align-items-center gap-3">
            <h2>Partners</h2>

            <p class="al-w pb-5 pb-lg-0">Leverage agile frameworks to provide a robust synopsis for high level overviews. Iterative approaches to corporate strategy.</p>
        
            <div class="al-row">
                <div class="al-col">
                    <img src="../assets/img/partner-2.png" alt="partner-2">
                </div>

                <div class="al-col al-light">
                    <img src="../assets/img/partner-3.png" alt="partner-3">
                </div>

                <div class="al-col al-book">
                    <img src="../assets/img/partner-4.png" alt="partner-4">
                </div>

                <div class="al-col">
                    <img src="../assets/img/partner-5.png" alt="partner-5">
                </div>

                <div class="al-col al-pen">
                    <img src="../assets/img/partner-6.png" alt="partner-6">
                </div>

                <div class="al-col al-trophy">
                    <img src="../assets/img/partner-8.png" alt="partner-8">
                </div>

                <div class="al-col al-paper">
                    <img src="../assets/img/partner-1.png" alt="partner-1">
                </div>

                <div class="al-col">
                    <img src="../assets/img/partner-7.png" alt="partner-7">
                </div>
            </div>
        </div>


        <div class="d-flex justify-content-end al-nm">
            <img class="al-wave" src="../assets/img/background-wave3.png" alt="wave">
        </div>
    </section>
</template>

<script>
    export default {
        name: "AppPartners"
    }
</script>

<style lang="scss" scoped>
    section{
        padding-top: 5rem;
    }
    .al-w{
        width: 100%;
    }

    .al-row{
        width: 90%;
        display: flex;
        justify-content: center;
        align-items: center;
        flex-wrap: wrap;
    }

    .al-col{
        width: calc(100% / 4);
        display: flex;
        justify-content: center;
        align-items: center;
        margin-top: -2.5rem;
        
        img{
            transform: scale(0.32);
            filter: opacity(0.4);
        }
    }

    .al-book{
        img{
            transform: scale(0.3) translateX(-55%);
        }
    }

    .al-paper{
        img{
            transform: scale(0.3) translateX(-50%);
        }
    }

    .al-light{
        img{
            transform: scale(0.3) translateX(-12%);
        }
    }

    .al-trophy{
        img{
            transform: scale(0.3) translateX(-25%);
        }
    }

    .al-wave{
        height: 125px;
    }

    .al-nm{
        margin-top: -3rem;
    }

    @media screen and (min-width: 576px){
        .al-col{
            img{
                transform: scale(0.4)
            }
        }

        .al-book{
        img{
            transform: scale(0.4) translateX(-55%);
        }
    }

    .al-paper{
        img{
            transform: scale(0.4) translateX(-50%);
        }
    }

    .al-light{
        img{
            transform: scale(0.4) translateX(-12%);
        }
    }

    .al-trophy{
        img{
            transform: scale(0.4) translateX(-25%);
        }
    }
    }

    @media screen and (min-width: 768px){
        .al-w{
            width: 75%;
        }

        .al-col{
            transform: scale(1.4);
        }

        .al-wave{
        height: 160px;
    }
    }

    @media screen and (min-width: 992px){
        .al-w{
            width: 60%;
        }

        .al-row{
            width: 80%;
        }

        .al-col{
            width: calc(100% / 8);
            transform: scale(0.8);
        }

        .al-pen{
            transform: scale(0.65) translateX(40%);
        }

        .al-trophy{
        img{
            transform: scale(0.4) translateX(-7%);
        }
    }

        .al-wave{
        height: 200px;
    }
    }

    @media screen and (min-width: 1200px){
        .al-w{
            width: 50%;
        }

        .al-col{
            transform: scale(0.9);
        }

        .al-pen{
            transform: scale(0.65) translateX(40%);
        }

        .al-wave{
            height: 240px;
        }

        .al-nm{
            margin-top: -4rem;
        }
    }

    @media screen and (min-width: 1400px){
        .al-col{
            transform: scale(1.05);
        }

        .al-pen{
            transform: scale(0.7) translateX(30%);
        }

        .al-wave{
            height: 280px;
        }

        .al-nm{
            margin-top: -4.5rem;
        }
    }
</style>