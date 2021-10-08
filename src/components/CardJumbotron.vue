<template>
    <div>
        <!--Jumbotron card topic based component-->
        <div class="topic_card_container">

        <!--div style not working, used img inside relative container
            and elements positioned inside it as absolute-->

            <img :src="topic.imgBgPath">
            
            <button class="bottom_left_topic btn btn-primary">{{topic.topic}}</button>
            <h6 class="bottom_left_title">{{topic.title}}</h6>

        </div>
           
        <!--attemps to make div style work-->
        
        <!-- <div :style="{ 'background-image': 'url(' + require(`../assets/img/${imgBgPath}`) + ')' }"></div> -->
        <!--<div v-bind:style="{ 'background-image': 'url(../assets/images/img/blog-46.jpg)' }"></div>-->
    
    </div>      
</template>

<script>
export default {
    name : 'CardJumbotron',
    props : ['topic'],
    data : function () {
        return {
     
    }
    }
}
</script>

<style scoped lang="scss">
@import "../style/variables.scss";

    img {
        width: 350px;
        height: 200px;
        object-fit: cover;
        filter: brightness(50%);
    }

    .topic_card_container {
        position: relative;
        margin-bottom: 30px;
    }

    .bottom_left_topic {
        position: absolute;
        bottom: 60px;
        left: 16px;
        color: $whiteColor;
        text-transform: uppercase;
        font-size: small;
        font-weight: bold;
    }

    .bottom_left_title {
        position: absolute;
        bottom: 8px;
        left: 16px;
        color: $whiteColor;
        font-weight: bold;
        text-transform: capitalize;
        padding-right: 5px;
    }
</style>