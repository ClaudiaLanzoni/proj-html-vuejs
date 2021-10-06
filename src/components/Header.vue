<template>
    <div>
        <!-- common blog specifications menu section-->
        <section> 
            
            <nav> 
                <p>Everything about Lifestyle, Travel and Gadgets!</p>

                <ul v-for="(element, index) in blog_specification_nav" :key="index">
                    <li>{{element}}</li>
                </ul>
            </nav>

        </section>

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
    ul {
        list-style-type: none;
        display: inline-block;
        text-transform: uppercase;
    }

    p {
        display: inline-block;
    }
</style>