<template>
   <header class="bg-light">
        <nav class="container d-flex justify-content-between py-4">
            <div>
                <img src="/img/dc-logo.png" alt="logo"/>
            </div>

            <ul class="d-flex align-items-center none-1">
                <li v-for="(items,index) in menu" :key="index" class="mx-2 fw-bold text-h none-1" role="button">
                    {{items}}
                    <div class="border-b"></div>
                </li>
            </ul>

            <div class="mt-4 none-1" id="search-container">
                <i class="fa-solid fa-magnifying-glass"></i>
                <input type="text" placeholder="Search" />
            </div>

            <div class="navbar" id="hamburgher-menu" @click="openMenu">
                <div class="container-fluid">
                    <button class="navbar-toggler" type="button" data-bs-toggle="collapse" data-bs-target="#navbarToggleExternalContent" aria-controls="navbarToggleExternalContent" aria-expanded="false" aria-label="Toggle navigation">
                    <span class="navbar-toggler-icon "></span>
                    </button>
                </div>

                <div class="dropdown mt-2">
                    <ul class="dropdown-menu" id="dropdown">
                        <li v-for="(items,index) in menu" :key="index" class="dropdown-item" >
                            {{items}}
                        </li>
                    </ul>
                </div>

            </div>
            
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
        },
        methods: {
            openMenu(){
                document.getElementById("dropdown").classList.toggle("show");
            }
        }
    }
</script>

<style lang="scss" scoped>
    .border-b{
        border:5px solid transparent;
    }
    .text-h:hover{
        color: #0C7CEC;
        .border-b{
        width: 100%;
        border-color:#0C7CEC;
        border-radius: 10px;
        transform: translate(0, 66px);
        transition: 0.5s ease-in-out;
        }
    }
    #search-container{
       position: relative;
        input{
            padding-left:25px;
            border: none;
            border-bottom: 2px solid #0C7CEC;
            outline: none;
            width: calc(100% - 25px);
            font-size: 15px;
            background-color: transparent;
        }
        i{
            position: absolute;
            left: 5px;
        }
    }
   
    #hamburgher-menu{
        display: none;
    }
    @media screen and (max-width: 991px) {
        .none-1{
            display: none;
        }
        #hamburgher-menu{
            display: block;
        }
    }
</style>