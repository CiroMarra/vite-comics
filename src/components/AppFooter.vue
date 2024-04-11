<script>
 export default {
    name: 'AppHeader',
     data() {
        return {
             dcComics: [
                 {
                     text: 'Characters',
                 },
                 {
                     text: 'Comics',
                 },
                 {
                     text: 'Movies',
                 },
                 {
                     text: 'TV',
                 },
                 {
                     text: 'Games',
                 },
                 {
                     text: 'Videos',
                 },
                 {
                     text: 'News',
                 },
             ],


             dcShop: [
                 {
                     text: 'Shop DC',
                 },
                 {
                     text: 'Shop DC Collectibles',
                 },
             ],

             dc: [
                 {
                     text: 'Terms Of Use',
                 },
                 {
                     text: 'Privacy policy (New)',
                 },
                 {
                     text: 'Ad Choices',
                 },
                 {
                     text: 'Advertising',
                 },
                 {
                     text: 'Jobs',
                 },
                 {
                     text: 'Subscriptions',
                 },
                 {
                     text: 'Talent Workshops',
                 },
                 {
                     text: 'CPSC Certificates',
                 },
                 {
                     text: 'Ratings',
                 },
                 {
                     text: 'Shop Help',
                 },
                 {
                     text: 'Contact Us',
                 },
             ],

             sites: [
                 {
                     text: 'Terms Of Use',
                 },
                 {
                     text: 'Privacy policy (New)',
                 },
                 {
                     text: 'Ad Choices',
                 },
                 {
                     text: 'Advertising',
                 },
                 {
                     text: 'Jobs',
                 },

             ],
         }
     },
    }

</script>

<template>
 <footer>
    <section class="ms-footer">
        
            <div class="container pt-5 d-flex">
                <div class="row flex-column">
                    <ul class="text-white"> DC COMICS
                        <li v-for="comics in dcComics">
                            <a href="#">{{ comics.text }}</a>
                        </li>
                    </ul>

                    <ul class="text-white"> SHOP
                            <li v-for="shop in dcShop">
                                <a href="#">{{ shop.text }}</a>
                            </li>
                    </ul>
                    
                
                </div> 
                <div>
                    <ul class="text-white"> DC
                            <li v-for="dcs in dc">
                                <a href="#">{{ dcs.text }}</a>
                            </li>
                    </ul>
                </div>
                <div>
                    <ul class="text-white"> SITES
                            <li v-for="site in sites">
                                <a href="#">{{ site.text }}</a>
                            </li>
                    </ul>
                </div>
                <div class="img-logo-footer d-flex position-relative">
                    <img src="../assets/img/dc-logo-bg.png" class="img-position">   
                </div> 
            </div>
    </section>


 </footer>

</template>

<style scoped lang="scss">

@use '../style/partials/variables.scss' as *;






</style>