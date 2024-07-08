<script>

    import AppFooter from './AppFooter.vue';
    import AppHeader from './AppHeader.vue';
    import AppMain from './AppMain.vue';

    export default {
        name: 'App',
        components: {
            AppHeader,
            AppMain,
            AppFooter,

        }
    }
</script>

<template>
    <AppHeader/>
    <AppMain :listCards="slider"/>
    <AppFooter/>
</template>

<style lang="scss" scoped>
@use '../src/styles/partials/_mixins.scss' as *;
@use '../src/styles/partials/_variables.scss' as *;
@use '../src/styles/general.scss';
@import url('https://fonts.googleapis.com/css2?family=Oswald:wght@200..700&display=swap');

* {
    font-family: "Oswald", sans-serif;
}
</style>