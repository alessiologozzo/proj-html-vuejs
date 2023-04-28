<template>
    <section>
        <div class="container">
            <div class="d-flex flex-column justify-content-center align-items-center">
                <img class="al-clock-img mb-4" src="../assets/img/Clock-and-Bell.png" alt="clock">
                <h2 class="al-bg-red mb-5">University Year</h2>
            </div>

            <div class="d-none d-sm-block mt-5">
                <div class="d-flex text-center">
                    <div class="al-w al-demo pb-1">
                        <h6>Demo Classes</h6>
                        <p>In the first week, students try to accomodate with the teaching style and choose their optional courses.</p>
                    </div>

                    <div class="al-w al-graduation pb-1">
                        <h6>Graduation Day</h6>
                        <p>On the day of graduation, all students gather for the ceremony and then network and party among others.</p>
                    </div>
                </div>

                <img class="al-timeline" src="../assets/img/Timeline-Item.png" alt="timeline">

                <div class="d-flex text-center">
                    <div class="al-w al-orientation pt-3">
                        <h6>Orientation</h6>
                        <p>First day of the university year, all students gather for the opening ceremony and then network with others.</p>
                    </div>

                    <div class="al-w al-evaluation pt-3">
                        <h6>Evaluation</h6>
                        <p>At the end of a semester, students take a general evaluation test for every subject they're learning.</p>
                    </div>
                </div>
            </div>

            <div class="d-sm-none text-center">

                <div class="col-12 pb-3">
                    <h6>Orientation</h6>
                    <p>First day of the university year, all students gather for the opening ceremony and then network with others.</p>
                </div>

                <div class="col-12 pb-3">
                    <h6>Demo Classes</h6>
                    <p>In the first week, students try to accomodate with the teaching style and choose their optional courses.</p>
                </div>

                <div class="col-12 pb-3">
                    <h6>Evaluation</h6>
                    <p>At the end of a semester, students take a general evaluation test for every subject they're learning.</p>
                </div>

                <div class="col-12 pb-3">
                    <h6>Graduation Day</h6>
                    <p>On the day of graduation, all students gather for the ceremony and then network and party among others.</p>
                </div>
            </div>
        </div>
    </section>
</template>

<script>
export default {
    name: "AppUniversity"
}
</script>

<style lang="scss" scoped>
@import "../assets/colors.scss";

section {
    margin-top: -0.5rem;
    padding-top: 5rem;
    background-color: $app_red;
    color: white;
}

.al-clock-img {
    width: 70px;
}

.al-bg-red {
    background-color: #db2a2c;
}

.al-timeline {
    width: 100%;
}

p{
    color: #f9d9da;
}

@media screen and (min-width: 576px) {
    .al-w {
        width: 200px;
    }

    .al-demo {
        transform: translateX(51%);
    }

    .al-graduation {
        transform: translateX(60%);
    }

    .al-orientation {
        transform: translateX(-2%);
    }

    .al-evaluation {
        transform: translateX(8%);
    }
}

@media screen and (min-width: 768px) {
    .al-w {
        width: 270px;
    }

    .al-demo {
        transform: translateX(50%);
    }

    .al-graduation {
        transform: translateX(55%);
    }

}

@media screen and (min-width: 992px) {
    .al-w {
        width: 350px;
    }

    .al-demo {
        transform: translateX(55%);
    }

    .al-graduation {
        transform: translateX(65%);
    }

    .al-orientation {
        transform: translateX(2%);
    }

    .al-evaluation {
        transform: translateX(11%);
    }
}

@media screen and (min-width: 1200px) {
    .al-w {
        width: 400px;
    }

    .al-demo {
        transform: translateX(60%);
    }

    .al-graduation {
        transform: translateX(72%);
    }

    .al-orientation {
        transform: translateX(4%);
    }

    .al-evaluation {
        transform: translateX(18%);
    }
}

@media screen and (min-width: 1400px) {
    .al-w {
        width: 450px;
    }

    .al-demo {
        transform: translateX(65%);
    }

    .al-graduation {
        transform: translateX(81%);
    }

    .al-orientation {
        transform: translateX(6%);
    }

    .al-evaluation {
        transform: translateX(24%);
    }
}
</style>