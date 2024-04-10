<template>
   <header class="bg-light">
     <nav class="container d-flex justify-content-between my-3">
        <div>
            <img src="/img/dc-logo.png" alt="logo"/>
        </div>
        <ul class="d-flex align-items-center">
            <li v-for="(items,index) in menu" :key="index" class="mx-3 fw-bold " :class="index === 2 ? 'text-info ' : ''">
                {{items}}
                <div :class="index === 2 ? 'st-blue-border' : ''"></div>
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
  .st-blue-border{
      width: 100%;
      height: 5px;
      background-color: rgb(0, 192, 128);
      border-radius: 10px;
  }
</style>