<template>
    <ul class="d-flex mt-3 align-items-center ">

        <h4 class="text-info mt-2 px-3">{{ title }}</h4>
        <li class="d-flex" v-for="(item,index) in items" :key="index">
            <a :href="item.url"> <i :class="item.name"></i> </a>
        </li>

    </ul>
</template>

<script>
    export default {
        name:'FollowLinks',
        props: ['title', 'items'],
    }
</script>

<style lang="scss" scoped>
    a{
        color: white;
    }
    i{
        color:rgb(168, 168, 168);
        font-size: 30px;
       padding: 0px 10px;
    }
    i:hover{
        color: white;
    }
</style>