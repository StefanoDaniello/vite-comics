<template>
   <main>
    <div class="bg-black">
        <div class="container p-5">
           <span class="bg-black text-white">--> Content goes here <--</span>
        </div>
    </div>
        <div class="bg-info ">
            <div class="container">
                <ul class="d-flex justify-content-center text-white">
                    <li v-for="(img,index) in shopimg" :key="index" class="m-3">
                        <div>
                            <img :src="img" alt=""/>
                        </div>
                    </li>
                    <li v-for="(items,index) in shop" :key="index" class="m-3">
                        {{items}}
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
                    '../assets/public/img/buy-comics-digital-comics.png',
                    '../assets/public/img/buy-comics-merchandise.png',
                    '../assets/public/img/buy-comics-subscriptions.png',
                    '../assets/public/img/buy-comics-shop-locator.png',
                    '../assets/public/img/buy-dc-power-visa.svg'
                ]
            }
        }
    }
</script>

<style lang="scss" scoped>
    ul{
        list-style: none;
    }
    span{
        font-size: 25px;
        font-weight: bold;
    }
    img{
        width: 100px;
    }
</style>