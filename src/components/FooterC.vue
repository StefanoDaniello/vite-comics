<template>
   <footer>
        <div id="footer-top" class="d-flex justify-content-around">
            <div class="p-5">
                <ul>
                    <li class="text-white">
                        <a href=""></a>
                    </li>
                </ul>
            </div>
            <div class="logo-width"></div>
        </div>
        <div id="footer-bottom" class="bg-dark">
            bdffgkjberfnbeffref
        </div> 
   </footer>
</template>

<script>
    export default {
        name: 'FooterC',
        data() {
            return {
                
            }
        }
    }
</script>

<style lang="scss" scoped>
    #footer-top{
        background-size: cover;
    }
    .logo-width{
        width: 563px;
        height: 370px;
        background-position: center;
        background-image: url('/img/dc-logo-bg.png');
    }
   
</style>