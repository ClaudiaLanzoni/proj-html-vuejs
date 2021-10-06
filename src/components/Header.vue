<template>
        <header>
        <div class="blog_specifications_nav_wrap">
            <div class="container">
                <!-- common blog specifications menu section-->
                <section> 
                    
                    <nav> 
                        <p>Everything about Lifestyle, Travel and Gadgets!</p>

                        <ul v-for="(element, index) in blog_specification_nav" :key="index">
                            <li>{{element}}</li>
                        </ul>
                    </nav>

                </section>
            </div>   
        </div> 

        <div class="container">
            <!-- blog logo section -->
            <section> 
                <img src="../assets/images/img/logo-default-slim.png" alt="Porto logo">
            </section>

            <!-- blog interaction menu section  -->

            <section>
                <nav>
                    <ul v-for="(element, index) in blog_interaction_nav" :key="index">
                            <li>{{element}}</li>
                    </ul>
                </nav>
            </section>
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
        blog_specification_nav: ['sign in', 'contact us', 'about us', 'contact us', 'buy now'],
        blog_interaction_nav : ['home', 'elements', 'features', 'pages', 'portfolio', 'blog', 'shop']
        }
    }
}
</script>

<style scoped lang="scss">
@import "../style/variables.scss";

    header {
        margin-bottom: 50px
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
    }
</style>