<template>
    <div class="al-lesson">
        
        <img :src="getUrl()" alt="err">

        <h6 class="pt-2 text-center">{{ lessonData.title }}</h6>

        <div class="d-flex justify-content-center gap-1">
            <i class="fa-regular fa-user pt-1"></i>
            <span>Teacher: {{ lessonData.teacher }}</span>
        </div>

        <div class="d-flex justify-content-center gap-1 pb-4">
            <i class="fa-solid fa-money-check-dollar pt-1"></i>
            <span>Price: {{ lessonData.price }}</span>
        </div>

        <a href="#" class="al-red-button">
            <i class="fa-solid fa-eye"></i>
            <span>View Course</span>
        </a>
    </div>
</template>

<script>
    export default {
        name: "AppLesson",

        props: {
            lessonData: {}
        },

        methods: {
            getUrl(){
                return new URL(this.lessonData.src, import.meta.url).href;
            }
        },
    }
</script>

<style lang="scss" scoped>
    @import "../assets/utilities.scss";

    .al-lesson{
        display: flex;
        justify-content: center;
        align-items: center;
        flex-flow: column nowrap;
        gap: 0.5rem;
        position: relative;
        padding: 2rem 0.3rem;
        box-shadow: 1px 2px 20px 5px #eaeaea;
        margin-bottom: 4rem;
        
    }

    img{
        width: 50%;
    }

    .al-red-button{
        display: flex;
        justify-content: center;
        align-items: center;
        gap: 0.4rem;
        position: absolute;
        bottom: 0;
        left: 50%;
        transform: translate(-50%, 50%);
        white-space: nowrap;
        box-shadow: 1px 2px 20px 5px #eaeaea;

        &:hover{
            transform: translate(-50%, 50%) scale(1.07);
        }
    }
</style>