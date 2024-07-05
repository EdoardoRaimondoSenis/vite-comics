<script>
    import AppFooter from './AppFooter.vue';
    import AppHeader from './AppHeader.vue';
    import AppMain from './AppMain.vue';

    export default {
        name: 'App',
        components: {
            AppMain,
            AppFooter,
            AppHeader
        }
    }
</script>

<template>
    
</template>

<style lang="scss" scoped>
@use '../src/styles/partials/_mixins.scss' as *;
@use '../src/styles/partials/_variables.scss' as *;
@use '../src/styles/general.scss';
</style>