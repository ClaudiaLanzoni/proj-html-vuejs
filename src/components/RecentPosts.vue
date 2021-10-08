<template>
  <div>
      <img :src="recentPost.imgPost" alt="post image">
        <div class="caption_img_post">
            <div class="title_style">{{recentPost.titlePost}}</div>
            <div class="date_style">{{recentPost.datePost}}</div>
        </div>
  </div>
</template>

<script>
export default {
    name : 'RecentPosts',
    props : ['recentPost'],
    data : function () {
        return {

        }
    }
}
</script>

<style lang="scss">
@import "../style/variables.scss";


</style>