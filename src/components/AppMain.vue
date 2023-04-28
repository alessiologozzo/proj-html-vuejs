<template>
    <main>
        <AppCourses />
        <AppFaculties />
        <AppUniversity />
        <AppEvents />
        <AppLatest />
        <AppEfficient />
        <AppVariable />
        <AppNewsletter />
        <AppPartners />
        <AppFooter />
    </main>
</template>

<script>
    import AppCourses from './AppCourses.vue';
    import AppFaculties from './AppFaculties.vue';
    import AppUniversity from './AppUniversity.vue';
    import AppEvents from './AppEvents.vue';
    import AppLatest from './AppLatest.vue';
    import AppEfficient from './AppEfficient.vue';
    import AppVariable from "./AppVariable.vue";
    import AppNewsletter from './AppNewsletter.vue';
    import AppPartners from './AppPartners.vue';
    import AppFooter from './AppFooter.vue';

    export default {
        name: "AppMain",

        components: {
            AppCourses,
            AppFaculties,
            AppUniversity,
            AppEvents,
            AppLatest,
            AppEfficient,
            AppVariable,
            AppNewsletter,
            AppPartners,
            AppFooter
        }
    }
</script>

<style lang="scss" scoped>
    
</style>