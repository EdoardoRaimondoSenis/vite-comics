<script>
import { createApp } from 'vue';

export default {
  
  name: 'AppHeader',
  data() {
    return {
      linkAdd: [
        { name: 'CHARACTERS' },
        { name: 'COMICS' },
        { name: 'MOVIES' },
        { name: 'TV' },
        { name: 'GAMES' },
        { name: 'COLLECTIBLES' },
        { name: 'VIDEOS' },
        { name: 'FANS' },
        { name: 'NEWS' },
        { name: 'SHOP' }
      ]
    };
  }
};
</script>

<template>
  <header>
    <div class="header">
      <img src="../public/dc-logo.png" alt="">
      <ul>
        <li class="link" v-for="element in linkAdd"><a href="">{{ element.name }}</a></li>
      </ul>
    </div>
  </header>
</template>

<style lang="scss" scoped>
@use '../src/styles/partials/_mixins.scss' as *;
@use '../src/styles/partials/_variables.scss' as *;
@use '../src/styles/general.scss';

.header {
  margin: 6rem 15% auto;
  display: flex;
  align-items: center;
  justify-content: space-between;
  padding: 15px 0;

  img {
    width: 5rem;
    height: 5rem;
  }

  ul {
    display: flex;
    list-style: none;
  }

  ul li a {
    padding: 2.35rem 15px;
    text-decoration: none;
    color: black;

    &:hover {
      transition: linear 100ms;
      border-bottom: 5px solid #0c7cec;
      color: #0c7cec;
    }
  }
}

</style>