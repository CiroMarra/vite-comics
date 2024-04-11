<script>
 export default {
    name: 'AppHeader',
     data() {
        return {
             links: [
                 {
                     text: 'CHARACTERS',
                     active: true
                 },
                 {
                     text: 'COMICS',
                     active: false
                 },
                 {
                     text: 'MOVIES',
                     active: false
                 },
                 {
                     text: 'TV',
                     active: false
                 },
                 {
                     text: 'GAMES',
                     active: false
                 },
                 {
                     text: 'COLLECTIBLES',
                     active: false
                 },
                 {
                     text: 'VIDEOS',
                     active: false
                 },
                 {
                     text: 'FANS',
                     active: false
                 },
                 {
                     text: 'NEWS',
                     active: false
                 },
                 {
                     text: 'SHOP',
                     active: false
                 },
             ],
         }
     },

     methods: {
        setActive(index) {
            this.links.forEach((link, i) => {
                link.active = i === index;
            });
        },
    },
 }
</script>

<template>
    <header>

        <div class="container-xxl">
            <nav class="navbar bg-body-tertiary">
                <div class="container-fluid">
                    <a class="navbar-brand" href="#">
                        <img src="../assets/img/dc-logo.png" alt="Logo" width="100" height="100" class="d-inline-block align-text-top">
                    </a>
                    <ul class="d-flex">
                        <li :class="{ 'active': link.active }" v-for="(link, index) in links" :key="index" @click="setActive(index)">
                            <a href="#">{{ link.text }}</a>
                        </li>
                    </ul>
                </div>
            </nav>
        </div>
 
    </header>

</template>

<style scoped lang="scss">

@use '../style/partials/variables' as *;


</style>