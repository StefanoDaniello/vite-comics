<template>
   <main>
        <div class="bg-black">
            <div class="container p-5">
            <h3 class="bg-black text-white p-1">--> Content goes here <--</h3>
            </div>
        </div>

        <div class="bg-info py-4">
            <div class="container">
                <ul class="d-flex">
                    <li v-for="(img,index) in shopimg" :key="index" class="m-3 d-flex justify-content-center align-items-center ">
                        <div class="shopimg-width">
                            <img :src="img" alt="shop-img"/>
                        </div>
                        <span class="mx-3">{{shop[index]}}</span>
                    </li>
                   
                </ul>
            </div>
        </div>
        
   </main>
</template>

<script>
    export default {
        name:'MainC',
        data() {
            return {
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
                ]
            }
        }
    }
</script>

<style lang="scss" scoped>
    span{
        font-size: 15px;
        color: #ffffff;
    }
    .shopimg-width{
        width: 60px;
    }
</style>