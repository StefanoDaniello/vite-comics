<template>

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

</template>

<script>
    export default {
        name: 'BlueSlideC',
        props: ['shop', 'shopimg'],
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