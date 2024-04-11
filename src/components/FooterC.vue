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
           <div class="container d-flex justify-content-between align-items-center py-2">
               <div class="text-white blue-border p-2" id="sign-button">
                   <a href="#">SIGN-UP NOW!</a> 
               </div>
               <div >
                   <FollowLinks :title="followlinks.title" :items="followlinks.items"/>
               </div>   
           </div>

        </div> 
   </footer>
</template>

<script>
    import LinksC from './LinksC.vue';
    import FollowLinks from './FollowLinks.vue';
    export default {
        name: 'FooterC',
        components: {
            LinksC,
            FollowLinks,
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
                    },
                },
                followlinks:{
                    title:'FOLLOW US',
                    items:[
                        {
                            name:'fa-brands fa-facebook',
                            url:'#'
                        },
                        {
                            name:'fa-brands fa-twitter',
                            url:'#'
                        },
                        {
                            name:'fa-brands fa-youtube',
                            url:'#'
                        },
                        {
                            name:'fa-brands fa-pinterest',
                            url:'#'
                        },
                        {
                            name:'fa-brands fa-periscope',
                            url:'#'
                        }
                    ]   
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
    .blue-border{
        border:2px solid rgb(0, 192, 176);
    }
    #footer-bottom{
       padding: 10px 0px;
    }
    #sign-button:hover{
        background-color: rgb(0, 192, 176);
        transition: 0.5s ease-in-out;
    }
</style>