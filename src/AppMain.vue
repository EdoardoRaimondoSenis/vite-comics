<script>
import ListCards from './components/listCards.vue';

    export default {
        name: 'AppMain',
        components: {
            ListCards
        }
    }
    
</script>

<template>
  <main>
    <ul>    
      
    </ul>
  </main>
</template>

<style lang="scss" scoped>
@use '../src/styles/partials/_mixins.scss' as *;
@use '../src/styles/partials/_variables.scss' as *;
@use '../src/styles/general.scss';

main {
    display: flex;
    align-items: center;
    background-color: black;
    height: 8rem;
    color: white;
    padding-left: 15%;
    padding-right: 15%;
    z-index: 10;
}

</style>