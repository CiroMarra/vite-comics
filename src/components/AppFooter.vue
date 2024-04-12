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
    <section class="ms-endfooter">
        <div class="container">
            <div class="d-flex justify-content-between align-items-center py-3">
            <div class="p-2 e"><button type="button" class="btn btn-outline-primary text-white">SIGN-UP NOW!</button></div>
            <div class="p-2 ms-auto text-white">FOLLOW US</div>
            <div class="p-2"><img src="../assets/img/footer-facebook.png" alt=""></div>
            <div class="p-2"><img src="../assets/img/footer-twitter.png" alt=""></div>
            <div class="p-2"><img src="../assets/img/footer-youtube.png" alt=""></div>
            <div class="p-2"><img src="../assets/img/footer-pinterest.png" alt=""></div>
            <div class="p-2"><img src="../assets/img/footer-periscope.png" alt=""></div>
        </div>
</div>
</section>


 </footer>

</template>

<style scoped lang="scss">
.ms-endfooter {
    background-color:#303030;
}

.ms-footer {
    background-image: url(./src/assets/img/footer-bg.jpg);
    height: 371px;
    background-repeat: no-repeat;
    background-size: cover;
    overflow-y: hidden;

    .img-logo-footer {

        .img-position {
        height: 532px;
        width: 600px;
        position: absolute;
        bottom: 1px;
        left: 300px;
        bottom: -90px;
    
    }
    
    }

    ul {
        list-style: none;
        font-weight: bolder;
    
    
        li {
    
            color: grey;
        }
    
        a {
            padding: 3px 1px;
            text-decoration: none;
            font-size: 12px;
            font-weight: lighter;
            color: lightgrey;
        }
        
        a:hover {
            color: white;
        }
    
     
    }



}






</style>