<script>
    export default {
        name: 'AppFooter',
        data() {
            return {
                shop: [
                    { 
                        name: 'DIGITAL COMICS',
                        icon: '../public/buy-comics-digital-comics.png'
                    },
                    { 
                        name: 'DC MERCHANDISE',
                        icon: '../public/buy-comics-merchandise.png'
                    },
                    { 
                        name: 'SUBSCRIPTION',
                        icon: '../public/buy-comics-subscriptions.png'
                    },
                    { 
                        name: 'COMIC SHOP LOCATOR', 
                        icon:'../public/buy-comics-shop-locator.png'
                    },
                    { 
                        name: 'DC POWER VISA', 
                        icon: '../public/buy-dc-power-visa.svg'
                    },
                ],

                dcComicsLinks: [
                    {
                        name: 'Characters'
                    },
                    {
                        name: 'Comics'
                    },
                    {
                        name: 'Movies'
                    },
                    {
                        name: 'TV'
                    },
                    {
                        name: 'Games'
                    },
                    {
                        name: 'Videos'
                    },
                    {
                        name: 'News'
                    },
                ],

                shopLinks: [
                    {
                        name: 'Shop DC'
                    },
                    {
                        name: 'Shop DC Collectibles'
                    },
                ],

                dcLinks: [
                    {
                        name: 'Terms Of Use'
                    },
                    {
                        name: 'Privacy Policy(New)'
                    },
                    {
                        name: 'Ad Choices'
                    },
                    {
                        name: 'Advertising'
                    },
                    {
                        name: 'Jobs'
                    },
                    {
                        name: 'Subscriptions'
                    },
                    {
                        name: 'Talent Workshops'
                    },
                    {
                        name: 'CPSC Certificates'
                    },
                    {
                        name: 'Ratings'
                    },
                    {
                        name: 'Shop Help'
                    },
                    {
                        name: 'Contact Us'
                    },
                ],

                sitesLinks: [
                    {
                        name: 'DC'
                    },
                    {
                        name: 'MAD Magazine'
                    },
                    {
                        name: 'DC Kids'
                    },
                    {
                        name: 'DC Universe'
                    },
                    {
                        name: 'DC Power Visa'
                    },
                ],

                socialLinks: [
                    {
                        icon: '../public/footer-facebook.png'
                    },
                    {
                        icon: '../public/footer-twitter.png'
                    },
                    {
                        icon: '../public/footer-youtube.png'
                    },
                    {
                        icon: '../public/footer-pinterest.png'
                    },
                    {
                        icon: '../public/footer-periscope.png'
                    },
                ],

            };
        }
    }
</script>

<template>
  <footer>
    <div class="shopLink">
        <ul class="listShop">
            <li v-for="element in shop"><img :src="element.icon" alt=""><a href="">{{ element.name }}</a></li>
        </ul>
    </div>
    <div class="footerLink">
        <div>
            <ul class="listLinkFooter">
                <h2 class="titleLinkFooter">DC COMICS</h2>
                <li v-for="element in dcComicsLinks"><a href="">{{ element.name }}</a></li>
            </ul>
            <ul class="listLinkFooter">
                <h2 class="titleLinkFooter">SHOP</h2>
                <li v-for="element in shopLinks"><a href="">{{ element.name }}</a></li>
            </ul>
        </div>
        <div>
            <ul class="listLinkFooter">
                <h2 class="titleLinkFooter">DC</h2>
                <li v-for="element in dcLinks"><a href="">{{ element.name }}</a></li>
            </ul>
        </div>
        <div>
            <ul class="listLinkFooter">
                <h2 class="titleLinkFooter">SITES</h2>
                <li v-for="element in sitesLinks"><a href="">{{ element.name }}</a></li>
            </ul>
        </div>
        <img class="logoBg" src="../public/dc-logo-bg.png" alt="">
    </div>
    <div class="followLinks">
        <div class="sign">SIGN-UP NOW!</div>
        <div class="follow">
            <ul>
                <li class="followUs">FOLLOW US</li>
                <li v-for="element in socialLinks"><a href=""><img :src="element.icon" alt=""></a></li>
            </ul>
        </div>
    </div>
  </footer>
</template>

<style lang="scss" scoped>
@use '../src/styles/partials/_mixins.scss' as *;
@use '../src/styles/partials/_variables.scss' as *;
@use '../src/styles/general.scss';

.shopLink {
    background-color: #0c7cec;
}

.listShop {
    display: flex;
    align-items: center;
    justify-content: center;
    margin: 0;
    padding: 1rem 0;

    li {
        display: flex;
        align-items: center;
        list-style: none;
        margin: 0 15px;
    }

    li img {
        width: 3rem;
        margin: 0 10px;
    }

    li a {
        text-decoration: none;
        color: white;
    }
}

.footerLink {
    position: relative;
    display: flex;
    background-image: url(../public/footer-bg.jpg);
    background-repeat: no-repeat;
    background-size: cover;
    padding: 2rem 15% 2rem 15%;


    .titleLinkFooter {
        color: white;
        margin: 10px 0;
    }

    .listLinkFooter {
        padding: 0 3rem 0 0;
        li {
            list-style: none;
        }

        a {
            text-decoration: none;
            color: gray;

            &:hover {
                transition: 200ms;
                color: lightgrey;
            }
        }
    }
    .logoBg {
        position: absolute;
        width: 35rem;
        right: 15%;
        top: -10%;
    }
}

.followLinks {
    position: relative;
    display: flex;
    align-items: center;
    justify-content: space-between;
    padding: 1rem 15% 1rem 15%;
    background-color: black;
    z-index: 10;

    .sign {
        color: white;
        padding: 15px;
        border: #0c7cec solid 1px;
        cursor: pointer;

        &:hover {
            background-color: #0c7cec;
            transition: 200ms;
        }
    }

    .followUs {
        color: #0c7cec;
        padding: 0 1rem;
        font-size: 20px;
        font-weight: 500;
        cursor: pointer;
    }

    ul {
        display: flex;
        align-items: center;
    }

    ul li {
        list-style: none;
        margin: 0 5px;
    }
}


</style>