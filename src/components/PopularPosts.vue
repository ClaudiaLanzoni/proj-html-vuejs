<template>
  <div>
        <img :src="popularPost.imgPost" alt="post image">
        <div class="caption_img_post">
            <div>{{popularPost.titlePost}}</div>
            <div>{{popularPost.datePost}}</div>
        </div>
  </div>
</template>

<script>
export default {
    name : 'PopularPosts',
    props : ['popularPost'],
    data : function () {
        return {

        }
    }
}
</script>

<style scoped lang="scss">
@import "../style/variables.scss";

</style>