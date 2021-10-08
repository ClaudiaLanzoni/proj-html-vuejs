<template>
        <header>

        <!-- Common blog specifications menu section-->
        <div class="blog_specifications_nav_wrap">
            <div class="container">
                <div class="row">
                    <div class="col-12">  
                        <nav> 
                            <p class="text-white">Everything about Lifestyle, Travel and Gadgets!</p>

                            <ul v-for="(element, index) in blog_specification_nav" :key="index">
                                <li class="text-white">{{element.command}}</li>
                            </ul>
                        </nav>
                    </div>
                </div>
            </div>   
        </div> 

        <!-- Blog logo section -->
        <div class="container">
            <div class="row">
                <div class="col-12 mb-5">
                    <div class="header_logo_section">
                        <img src="../assets/images/img/logo-default-slim.png" alt="Porto logo">
                    </div>
                </div>
            </div>
         </div>    

        <!-- Blog interaction menu section  -->
        <div class="menu_wrap">
            <nav>
                <div class="container">
                    <div class="row">
                        <div class="col-12">
                            <div class="d-inline" v-for="(element, index) in blog_interaction_nav" :key="index">
                                <h6 class="h6_style">{{element.link}}</h6>
                            </div>
                        </div>
                    </div>
                </div>
            </nav>
        </div>
       
    </header>

    
</template>

<script>
export default {
    name : 'Header',
    props : {

    },
    data : function () {
        return {
            blog_specification_nav: [
            {
                command : 'sign in'
            },
            {
                command : 'contact us'
            },
            {
                command : 'about us'
            },
            {
                command : 'contact us'
            },
            {
                command : 'buy now'
            }
            ],

            blog_interaction_nav : [
            {
                link : 'home'
            },
            {
                link : 'elements'  
            },
            {
                link : 'features'
            },
            {
                link : 'pages'
            },
            {
                link : 'portfolio'
            },
            {
                link : 'blog',
            },
            {
                link : 'shop'
            }
            ]
        }
    }
}
</script>

<style scoped lang="scss">
@import "../style/variables.scss";

    header {
        font-size: 12px;
    }

    ul {
        list-style-type: none;
        display: inline-block;
        text-transform: uppercase;
    }

    p {
        display: inline-block;
    }

    .blog_specifications_nav_wrap {
        background-color: $headerBg;
        height: 50px;
        line-height: 50px;
    }

    h6 {
        display: inline-block;
        margin-right: 35px;

        &:hover {
            color: $headerBg;
        }
    }

    .header_logo_section {
        height: 50px;
        line-height: 100px;

        img {
            width: 7%;
        }
    }

    .menu_wrap {
        height: 50px;
        line-height: 50px;
        border-top: 1px solid rgb(199, 191, 191);
    }
</style>