<template>
   <main>
        <div class="bg-black ">
            <div id="jumbo">
                <img src="/img/jumbotron.jpg" alt="">
            </div>
            <div class="button-blue d-flex justify-content-center align-items-center">
                <h2>CURRENT SERIES</h2>
            </div>
            <div class="container">
              <div class="row ">
                <div class="col-12 col-md-6 col-lg-3 my-3" v-for="(item,index) in comix" :key="index">
                    <CardComponents :item="item" @elimina="Elimina(index)"/>
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
        emits: ['add'],
        data() {
            return {
                comix,
                shop:false,
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
        methods: {
            Elimina(index){
               this.comix.splice(index,1)
            }
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
   .button-blue{
       width: 300px;
       height: 80px;
       color: white;
       background-color: #0282F9;
       border: 2px solid white;
       border-radius: 10px;
       transform: translate(50%, -50%);
   }
</style>