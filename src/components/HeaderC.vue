<template>
   <header class="bg-light">
     <nav class="container d-flex justify-content-between my-2">
        <div>
            <img src="/img/dc-logo.png" alt="logo"/>
        </div>
        <ul class="d-flex align-items-center">
            <li v-for="(items,index) in menu" :key="index" class="mx-3">
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
  
</style>