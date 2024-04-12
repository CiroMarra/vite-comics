<script>
export default {
    name: 'ProductCard',
    props: {
        cardInfo: Object
    },
    methods: {
        getImageUrl(name) {
            return new URL(`${name}`, import.meta.url).href
        }
    }
}
</script>

<template>
    <div class="col-xl-2">
        <div class="img-container">
            <img :src="getImageUrl(cardInfo.thumb)"  :alt="cardInfo.series">
        </div>
        <div class="text-white pt-4">{{ cardInfo.series }}</div>
    </div>
</template>

<style scoped lang="scss">
@use '../style/partials/variables' as *;

.img-container {
    width: 170px;
    height: 170px;

    img {
        width: 100%;
        height: 100%;
        object-fit: cover;
        object-position: top;
    }
}
</style>