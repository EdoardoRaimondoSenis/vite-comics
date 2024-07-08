<script>
import ListCards from './listCards.vue';

    export default {
        name: 'AppMain',
        components: {
          ListCards
        },
        data() {
        return {
          slider: [
            {
              "thumb": "https://www.coverbrowser.com/image/action-comics/1-1.jpg",
              "price": "$19.99",
              "series": "Action Comics",
              "type": "comic book",
            },
            {
              "thumb": "https://www.panini.it/media/catalog/product/cache/a5b5dd3adfe0d321084804c738f29601/M/1/M1BLLA015ISBN_0.jpg",
              "price": "$3.99",
              "series": "American Vampire 1976",
              "type": "comic book",
            },
            {
              "thumb": "https://media.wired.com/photos/593384dad80dd005b42b2817/master/w_2560%2Cc_limit/Aquaman-16.jpg",
              "price": "$16.99",
              "series": "Aquaman",
              "type": "graphic novel",
            },
            {
              "thumb": "https://d29xot63vimef3.cloudfront.net/image/batgirl/1-1.jpg",
              "price": "$2.99",
              "series": "Batgirl",
              "type": "comic book",
            },
            {
              "thumb": "https://static.posters.cz/image/750/locandine-film-in-plexiglass-batman-prowl-comic-cover-i69653.jpg",
              "price": "$3.99",
              "series": "Batman",
              "type": "comic book",
            },
            {
              "thumb": "https://static.wikia.nocookie.net/marvel_dc/images/5/50/Batman_Beyond_v.1_1.jpg",
              "price": "$2.99",
              "series": "Batman Beyond",
              "type": "comic book",
            },
            {
              "thumb": "https://static.wikia.nocookie.net/marvel_dc/images/0/0d/Batman_Superman_Vol_1_1.jpg",
              "price": "$3.99",
              "series": "Batman/Superman",
              "type": "comic book",
            },
            {
              "thumb": "https://static.wikia.nocookie.net/marvel_dc/images/c/cf/Batman_Superman_Annual_Vol_2_1.jpg",
              "price": "$4.99",
              "series": "Batman/Superman Annual",
              "type": "comic book",
            },
            {
              "thumb": "https://static.wikia.nocookie.net/marvel_dc/images/5/54/Batman_The_Joker_War_Zone_Vol_1_1.jpg",
              "price": "$5.99",
              "series": "Batman: The Joker War Zone",
              "type": "comic book",
            },
            {
              "thumb": "https://static.wikia.nocookie.net/marvel_dc/images/6/64/Batman_Three_Jokers_Collected.jpg",
              "price": "$6.99",
              "series": "Batman: Three Jokers",
              "type": "comic book",
            },
            {
              "thumb": "https://static.wikia.nocookie.net/marvel_dc/images/f/f8/Batman_White_Knight_Presents_Harley_Quinn_Vol_1_1.jpg",
              "price": "$4.99",
              "series": "Batman: White Knight Presents: Harley Quinn",
              "type": "comic book",
            },
            {
              "thumb": "https://static.wikia.nocookie.net/marvel_dc/images/c/c8/Catwoman_Vol_2_1.jpg",
              "price": "$16.99",
              "series": "Catwoman",
              "type": "graphic novel",
            },
          ],
        };
      }
    }
    
</script>

<template>
  <main>
    <div class="imgMain">
      <div class="title">CURRENT SERIES</div>
    </div>
    <div class="containerCards">
      <ListCards v-for="(element, el) in slider" :key="el"
        :details="element"
      />
      <a href="" class="loadMore">LOAD MORE</a>
    </div>
    
  </main>
</template>

<style lang="scss" scoped>
@use '../src/styles/partials/_mixins.scss' as *;
@use '../src/styles/partials/_variables.scss' as *;
@use '../src/styles/general.scss';

main {
  position: relative;
  display: flex;
  flex-direction: column;
  align-items: center;
  color: white;


  .imgMain {
    background-image: url(../../public/jumbotron.jpg);
    background-size: cover;
    background-repeat: no-repeat;
    width: 100%;
    height: 25rem;

      .title {
      position: absolute;
      top: 23.5rem;
      left: 15%;
      padding: 5px 30px;
      background-color: #0c7cec;
      font-size: 30px;
    }


  }

  .containerCards {
    display: flex;
    flex-wrap: wrap;
    background-color: black;
    padding: 1rem 15% 3rem 15% ;
  }

  .loadMore {
    margin: 4rem calc(50% - 98px) 0 calc(50% - 98px);
    text-decoration: none;
    color: white;
    background-color: #0c7cec;
    padding: 10px 55px;
    border-radius: 5px;
    font-size: 20px;
  }


}

</style>