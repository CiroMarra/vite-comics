<script>
import AppProductsList from './AppProductsList.vue';
export default {
    name: 'AppMain',
    data() {
        return {
            cards: [
                {
                    img: 'buy-comics-digital-comics.png',
                    text: 'DIGITAL COMICS' 
                },
                {
                    img: 'buy-comics-merchandise.png',
                    text: 'DC MERCHANDISE' 
                },
                {
                    img: 'buy-comics-subscriptions.png',
                    text: 'SUBCRIPTION' 
                },
                {
                    img: 'buy-comics-shop-locator.png',
                    text: 'COMIC SHOP LOCATOR' 
                },
                {
                    img: 'buy-dc-power-visa.svg',
                    text: 'DC POWER VISA' 
                },
            ]
        };
    },
    methods: {
        getImageUrl(img) {
            return new URL(`../assets/img/${img}`, import.meta.url).href;
        }
    }
}
</script>

<template>
    <main>
    <section class="card-shop">
        <div class="container-fluid d-flex align-items-center justify-content-center ms-background-card"> 
            <div class="container">
                <div class="container text-center">
                    <div class="row align-items-center">
                        <div class="col" v-for="(card, index) in cards" :key="index">
                            <div class="mt-5 mb-5" style="max-width: 540px;">
                                <div class="row g-0 d-flex align-items-center justify-content-center">
                                    <div class="col-md-4">
                                        <img :src="getImageUrl(card.img)" class="img-fluid rounded-start ms-img" alt="...">
                                    </div>
                                    <div class="col-md-8">
                                        <div class="card-body">
                                            <p class="card-text text-white font">{{ card.text }}</p>
                                        </div>
                                    </div>
                                </div>
                            </div>
                        </div>
                    </div>
                </div>
            </div>
        </div>
    </section>
        
    </main>
</template>

<style scoped lang="scss">
    @use '../style/partials/variables' as *;
    .ms-background {
    background-color: #1c1c1c;
    height: 200px;
    
    .ms-text {
        color: white;
        font-size: 42px;
    }
}

.ms-background-card {
    background-color: #0282f9;
} 

.ms-img {
        height: 90px;
        width: 70px;
}

.font {
    font-size: 14px;
}

</style>