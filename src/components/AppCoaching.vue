<template>
    <div class="al-coaching">
        <h3>Coaching Sessions</h3>
        <i>{{ date }}</i>
        <p>Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor[...]</p>

        <div class="al-red-button">
            <i class="fa-solid fa-plus"></i>
            <a href="#">Find More</a>
        </div>
    </div>
</template>

<script>
    export default {
        name: "AppCoaching",

        props: {
            date: String
        }
    }
</script>

<style lang="scss" scoped>
    @import "../assets/utilities.scss";

    .al-coaching{
        display: flex;
        justify-content: center;
        align-items: center;
        flex-flow: column nowrap;
        gap: 0.6rem;
        position: relative;
        background-color: white;
        border-radius: 6px;
        color: #70727e;
        padding: 2rem;
        margin-bottom: 4rem;
        text-align: center;
    }

    a{
        color: white;
        text-decoration: none;

        &:hover{
            color: white;
        }
    }

    h3{
        color: #3d404f;
    }

    i{
        font-size: 0.9rem;
    }

    .al-red-button{
        position: absolute;
        bottom: 0;
        left: 50%;
        transform: translate(-50%, 50%);
        border: 1px solid #cc5454;
        display: flex;
        justify-content: center;
        align-items: center;
        gap: 0.5rem;
        box-shadow: 1px 10px 20px 2px #cc5454;
        white-space: nowrap;

        i{
            font-size: 1.1rem;
        }

        &:hover{
            transform: translate(-50%, 50%) scale(1.07);
        }
    }
</style>