<template>
    <div class="size_container">
        <!--
        <span class="small_container_img">
            <img class="img-fluid" :src="smallimg.img" alt="blog small image">
        </span>-->
    </div>
</template>

<script>
export default {
    name : 'CardPostTravel',
    props : ['smallimg'],
    data : function () {
        return {

    

        }
    }
}
</script>

<style scoped lang="scss">
@import "../style/variables.scss";

.size_container {
    width: 150px;
    height: 100px;
}

.small_container_img {

    img {
    width: 50px;
    height: 50px;
    display: inline-block;

}
}



</style>