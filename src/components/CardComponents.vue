<template>
   <div class="card" >
        <img :src="item.thumb"  :alt="item.series">
        <div class="card-body">
            <h5 class="card-title">{{item.series}}</h5>
            <p class="card-text">{{ item.type }}</p>
            <p class="card-text">{{ item.price }}</p>
            <a href="#" class="btn btn-primary">Go somewhere</a>
        </div>
    </div>
</template>

<script>

    export default {
        name:'CardComponents',
        props: ['item'],
    }
</script>

<style lang="scss" scoped>
   .card{
       height: 700px;
   }
   @media screen and (max-width: 768px) {
    .card{
        height: 100%;
    }
   }
</style>