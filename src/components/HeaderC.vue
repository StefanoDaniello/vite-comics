<template>
   <header class="bg-light">
     <nav class="container d-flex justify-content-between">
        <div>
            <img src="../assets/public/img/dc-logo.png" alt="logo"/>
        </div>
        <ul class="d-flex">
            <li v-for="(items,index) in menu" :key="index" class="m-3">
                {{items}}
            </li>
        </ul>
     </nav>
   </header>
</template>

<script>
    export default {
        name: 'HeaderC',
        data() {
            return {
                menu:[
                    'CHARACTERS',
                    'COMICS',
                    'MOVIES',
                    'TV',
                    'GAMES',
                    'COLLECTIBLES',
                    'VIDEOS',
                    'FANS',
                    'NEWS',
                    'SHOP'
                ]
            }
        }
    }
</script>

<style lang="scss" scoped>
   ul{
        list-style: none;
    }
</style>