<template>
   <div class="card" >
        <div class="card-img">
            <img :src="item.thumb"  :alt="item.series">
        </div>
        <div class="card-body">
            <h6 class="card-title">{{item.series}}</h6>
            <p class="card-text">{{ item.type }}</p>
            <p class="card-text">{{ item.price }}</p>
            <button class="btn btn-primary m-2" @click="addshop">Compra</button>
            <button class="btn btn-danger m-2" @click="$emit('elimina')">Elimina</button>
        </div>
    </div>
    <div id="compra" :class="(shop ? 'd-block' : 'd-none')">
        <h1>COMPRATO</h1>
    </div>
</template>

<script>

    export default {
        name:'CardComponents',
        props: ['item'],
        data() {
            return {
                shop:false
            }
        },
        methods: {
            addshop(){
                this.shop = true
            }
        }
    }
</script>

<style lang="scss" scoped>
    img{
        height: 100%;
    }
   .card{
       height: 700px;
       background-color: black;
       color: white;
    }
    #compra{
        display: none;
        height: 100%;
        background-color: rgba(180, 180, 180, 0.3);
        position: relative;
        top: -100%;
        h1{
            color: white;
            position: absolute;
            font-size: 100px;
            transform: rotate(-75deg);
           display: flex;
           justify-content: center;
           align-items: center;
           width: 100%;
           height: 100%;
        }
    }
   .card-img{
       height: 500px;
   }
   @media screen and (max-width: 768px) {
    .card{
        height: 100%;
    }
   }
</style>