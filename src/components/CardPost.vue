<template>
    <div class="post_container mb-5">
        <img class="img-fluid mb-3" :src="post.img" alt="post image">
        
        <!--pagina calendario-->
        <div>

        </div>

        <h3 class="mb-3">{{post.postTitle}}</h3>

        <p>{{post.textContent}}</p>

        <!-- autore, commenti -->
        <div>

        </div>

        

    </div>
</template>

<script>


export default {
    name : 'CardPost',
    props : ['post'],
    components : {
 
    },
    data : function () {
        return {
        
    }
    }
}
</script>

<style scoped lang="scss">
@import "../style/variables.scss";

</style>