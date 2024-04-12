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
        <div class="container-fluid">
            <nav class="navbar">
                <div class="container">
                    <a class="navbar-brand" href="#">
                        <img src="../assets/img/dc-logo.png" alt="Logo" class="d-inline-block align-text-top">
                    </a>
                    <ul class="d-flex">
                        <li  class="py-5":class="{ 'active': link.active }" v-for="(link, index) in links" :key="index" @click="setActive(index)">
                            <a href="#">{{ link.text }}</a>
                        </li>
                    </ul>
                </div>
            </nav>
        </div>
    </header>

</template>

<style scoped lang="scss">



nav {
    margin: 0;
    padding: 0;
    ul {

        margin: 0;
    
    
        li {
            padding: 8px;
            list-style: none;
           
            
    
    
            &.active{
                border-bottom: 4px solid #0282f9;

    
                a {
                    color: #0282f9;
                }
             
             }
        }
    
        a {
    
            text-decoration: none;
            font-weight: bolder;
            color: black;
            font-size: 15px;
        }
    
     
    }
}



</style>