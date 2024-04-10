<template>
   <footer>
        <div id="footer-top" class="d-flex justify-content-around align-items-center ">
        <div class="d-flex">
            <div class="px-2">
                <LinksC :title="links.dccomics.title" :items="links.dccomics.items"/>
                <LinksC :title="links.shop.title" :items="links.shop.items"/>
            </div>
            <div class="d-flex">
                <LinksC :title="links.dc.title" :items="links.dc.items"/>
                <LinksC :title="links.sites.title" :items="links.sites.items"/>
            </div>
        </div>
        
           

            <div class="logo-bg"></div>
        </div>
        <div id="footer-bottom" class="bg-dark">
            bdffgkjberfnbeffref
        </div> 
   </footer>
</template>

<script>
    import LinksC from './LinksC.vue';
    export default {
        name: 'FooterC',
        components: {
            LinksC,
        },
        data() {
            return {
                links:{
                    dccomics:{
                        title:'DC COMICS',
                        items:[
                            {
                                name:'Characters',
                                url:'#'
                            },
                            {
                                name:'Characters',
                                url:'#'
                            },
                            {
                                name:'Characters',
                                url:'#'
                            },
                            {
                                name:'Characters',
                                url:'#'
                            },
                            {
                                name:'Characters',
                                url:'#'
                            },
                            {
                                name:'Characters',
                                url:'#'
                            },
                            {
                                name:'Characters',
                                url:'#'
                            },
                            
                        ]
                    },
                    shop:{
                        title:'SHOP',
                        items:[
                            {
                                name:'Shop DC',
                                url:'#'
                            },
                            {
                                name:'Shop DC Collectibles',
                                url:'#'
                            },
                            
                        ]
                    },
                    dc:{
                        title:'DC',
                        items:[
                            {
                                name:'Characters',
                                url:'#'
                            },
                            {
                                name:'Characters',
                                url:'#'
                            },
                            {
                                name:'Characters',
                                url:'#'
                            },
                            {
                                name:'Characters',
                                url:'#'
                            },
                            {
                                name:'Characters',
                                url:'#'
                            },
                            {
                                name:'Characters',
                                url:'#'
                            },
                            {
                                name:'Characters',
                                url:'#'
                            },
                            
                        ]
                    },
                    sites:{
                        title:'SITES',
                        items:[
                            {
                                name:'Characters',
                                url:'#'
                            },
                            {
                                name:'Characters',
                                url:'#'
                            },
                            {
                                name:'Characters',
                                url:'#'
                            },
                            {
                                name:'Characters',
                                url:'#'
                            },
                            {
                                name:'Characters',
                                url:'#'
                            }
                        ]
                    }
                }
            }
        }
    }
</script>

<style lang="scss" scoped>
    #footer-top{
        background-size: cover;
    }
    .logo-bg{
        width: 563px;
        height: 370px;
        background-position: center;
        background-image: url('/img/dc-logo-bg.png');
    }
    
    #footer-bottom{
        height: 100px;
    }
</style>