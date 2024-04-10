<template>
    <ul class="text-secondary">

        <h3 class="text-white">{{ title }}</h3>
        <li class="d-flex flex-column" v-for="(item,index) in items" :key="index">
            <a :href="item.url">{{item.name}}</a>
        </li>

    </ul>

</template>

<script>
    export default {
        name: 'LinksC',
        props: ['title', 'items'],
    }
</script>

<style lang="scss" scoped>
    a:hover{
        text-decoration: underline;
        color: white;
    }
</style>