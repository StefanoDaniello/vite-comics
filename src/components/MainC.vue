<template>
   <main>
        <div class="bg-black ">
            <div id="jumbo">
                <img src="/img/jumbotron.jpg" alt="">
            </div>

            <div class="container">
              <div class="row ">
                <div class="col-12 col-md-6 col-lg-3 my-3" v-for="(item,index) in comix" :key="index">
                    <CardComponents :item="item"/>
                    <!-- passare un immagine una serie un tipo e un prezzo -->
                </div>
              </div>
            </div>

        </div>
        <BlueSlideC :shop="shop" :shopimg="shopimg"/>
   </main>
</template>

<script>
import BlueSlideC from './BlueSlideC.vue';
import {comix} from '../data/store.js';
import CardComponents from './CardComponents.vue';
    export default {
        name:'MainC',
        components: {
            BlueSlideC,
            CardComponents,
        },
        data() {
            return {
                comix,
                shop:[
                   'DIGITAL COMICS',
                   'DC MERCHANDISE',
                   'SUBSCRIPTION',
                   'COMIC SHOP LOCATOR',
                   'DC POWER VISA'
                ],
                shopimg:[
                    '/img/buy-comics-digital-comics.png',
                    '/img/buy-comics-merchandise.png',
                    '/img/buy-comics-subscriptions.png',
                    '/img/buy-comics-shop-locator.png',
                    '/img/buy-dc-power-visa.svg'
                ],
            }
        },
        mounted(){
           console.log(this.comix)
        },
    }
</script>

<style lang="scss" scoped>
   #jumbo{
       width: 100%;
       height: 600px;
       img{
           width: 100%;
           height: 100%;
       }
   }
   .st-card{
       width: 100%;
       height: 400px;
       border: 2px solid transparent;
   }
   .st-card:hover{
       box-shadow: 0 0 10px 5px rgb(1, 190, 175);
       transition: ease-in-out 0.5s;
       border-color:rgb(255, 255, 255);
    }
</style>