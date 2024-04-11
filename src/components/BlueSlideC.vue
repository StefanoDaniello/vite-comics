<template>

     <div class="bg-info py-4">
        <div class="container">
            <div class="row">
                <div v-for="(img,index) in shopimg" :key="index" class=" col-5 col-md-5 col-lg-2  mx-3 d-flex align-items-center">
                    <div class="shopimg-width">
                        <img :src="img" alt="shop-img"/>
                    </div>
                    <span class="mx-3">{{shop[index]}}</span> 
                </div>
                
            </div>
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