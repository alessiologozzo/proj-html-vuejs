<template>
    <div @click="changeActive()" :class="{'al-active': isActive()}">
        <img :src="getUrl()" alt="err" :class="{'img-filter': isActive()}">
        <div v-if="isActive()" class="al-clip"></div>
        <h5 class="mt-3">{{ cardData.name }}</h5>
    </div>
</template>

<script>
    export default {
        name: "FacultyCard",

        props: {
            cardData: { name: String,
                        src: String},
            cardIndex: Number,
            cardActive: Number
        },

        methods: {
            getUrl(){
                return new URL(this.cardData.src, import.meta.url).href;
            },

            isActive(){
                let result = false;

                if(this.cardIndex == this.cardActive)
                    result = true;

                return result;
            },

            changeActive(){
                this.$emit("activeChanged", this.cardIndex);
            }
        },
    }
</script>

<style lang="scss" scoped>
    @import "../assets/colors.scss";

    div{
        height: 100%;
        display: flex;
        flex-flow: column nowrap;
        align-items: center;
        text-align: center;
        color: $app_red;
        padding: 1rem 2.5rem;
        cursor: pointer;
        position: relative;

        &:hover{
            background-color: #e1e1e1;
        }

        &:hover.al-active{
            background-color: $app_red;
        }
    }

    img{
        width: 100%;
    }

    .img-filter{
        filter: brightness(0) invert(100%);
    }

    .al-clip{
        width: 20px;
        height: 50px;
        background-color: $app_red;
        clip-path: polygon(50% 0, 100% 50%, 50% 100%, 0 50%);
        position: absolute;
        bottom: -15px;
        left: 50%;
        transform: translateX(-50%);
    }

    h5{
        z-index: 1;
    }
</style>