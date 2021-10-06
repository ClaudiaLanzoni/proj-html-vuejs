<template>
    <div>

        <div class="topic_container">
            <img :src="topic.imgBgPath">
            <div>{{topic.topic}}</div>
            <div>{{topic.title}}</div>
        
       <!--
           <div :style="{ 'background-image': `url(${element.src})` }"></div>
           <img :src="element.src">
            <div v-bind:style="{ 'background-image': 'url(../assets/images/img/blog-46.jpg)' }"></div>
        -->
        </div>
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

.topic_container {
    width: 200px;
    height: 200px;
    border: 3px solid black;

    img {
        width: 70%;
        height: 50%;
    }
}

</style>