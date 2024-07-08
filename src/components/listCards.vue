<script>

export default {
    name: 'ListCards',
    props: {
        details: Object
    }
}
</script>

<template>
    <div class="card">
            <img :src="details.thumb" alt="">
            <h2>{{ details.series }}</h2>
        </div>
</template>

<style lang="scss">

.card {
    width: calc(100% / 6 - 2rem);
    height: 17rem;
    margin: 0 1rem;

    img {
        width: 10rem;
        height: 13rem;
    }
}


</style>