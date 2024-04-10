<template>
   <main>
        <div class="bg-black">
            <div class="container p-5">
                <h3 class="bg-black text-white p-1" role="button" @click="jumbo">--> Content goes here <--</h3>
            </div>
            <div :class="(prova ? 'd-none' : 'd-block')">
                <div id="jumbo">
                    <img src="/img/jumbotron.jpg" alt="">
                </div>

                <div class=" container d-flex justify-content-center align-items-center py-5">
                    <div class="row g-3">
                        <div class="col-3" v-for="(card,index) in cardcontent" :key="index">
                            <img :src="card" alt="ciao" class="rounded-4 st-card">
                        </div>
                    </div>
                </div>
               

            </div>
        </div>
        <BlueSlideC :shop="shop" :shopimg="shopimg"/>
   </main>
</template>

<script>
import BlueSlideC from './BlueSlideC.vue';
    export default {
        name:'MainC',
        components: {
            BlueSlideC,
        },
        data() {
            return {
                prova: true,
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
                cardcontent:[
                    'img/batmancontent.jpeg',
                    'img/flashcontent.jpeg',
                    'img/batman2content.jpeg',
                    'img/flash2content.jpeg',
                    'img/thorcontent.jpeg',
                    'img/hulkcontent.jpeg',
                    'img/thor2content.jpeg',
                    'img/hulk2content.jpeg',

                ]
            }
        },
        methods: {
            jumbo(){
                if(this.prova){
                    this.prova=false;
                }else{
                    this.prova=true;
                }
            }
        },
    }
</script>

<style lang="scss" scoped>
   .st-card{
       width: 100%;
       height: 400px;
       border: 2px solid transparent;
   }
   .st-card:hover{
       box-shadow: 0 0 10px 5px rgb(1, 190, 175);
       transition: all 0.5s;
       border-color:rgb(255, 255, 255);
    }
</style>