<template>
    <main>
       <!-- Jumbotron section with topic-based content cards -->
      <div class="jumbotron_container mb-5">
        <div class="container">
            <div class="row">
              <CardJumbotron class="col-4 d-flex justify-content-between" 
              v-for="(element, index) in topicCard" :key="index" :topic="element"/>
            </div>
        </div>
      </div>

      <!-- Posts collection section -->
      <PostsCollection />

      <!-- Blog's topics button section-->
      <TagsCollection />
      
      
    <!-- Main cards section -->
      <div class="container">
        <div class="row">
          <div class="col-8">
          <!-- Content cards section -->
            <CardPost
            v-for="(element, index) in postsCard" :key="index" :post="element"/>

          <!-- Larger Travel content card -->
            <CardPostTravel />

          <!-- Bottom pages section -->
            <div class="pages_box mb-4">
                <a href="#">&lt;</a>
                <a href="#">1</a>
                <a href="#">2</a>
                <a href="#">3</a>
                <a href="#">&gt;</a>
            </div>
          </div>

          <AsideSocialMedia class="col-4"/>
        </div>

      </div>

      
    </main>
</template>

<script>
import CardJumbotron from './CardJumbotron.vue';
import PostsCollection from './PostsCollection.vue';
import TagsCollection from './TagsCollection.vue'
import CardPost from './CardPost.vue';
import CardPostTravel from './CardPostTravel.vue';
import AsideSocialMedia from './AsideSocialMedia.vue';

export default {
  name: 'Main',
  props: {

  },
  components: {
    CardJumbotron,
    PostsCollection,
    TagsCollection,
    CardPost,
    CardPostTravel,
    AsideSocialMedia
  },
  data : function () {
    return {
      topicCard : [
        { 
        imgBgPath : require('../assets/images/img/blog-46.jpg'),
        topic : 'photography',
        title : 'how to take better concert pictures in 30 seconds',
        },
        { 
        imgBgPath : require('../assets/images/img/blog-47.jpg'),
        topic : 'gadgets',
        title : 'gadgets that make your smartphone even smarter'
        },
        { 
        imgBgPath : require('../assets/images/img/blog-48.jpg'),
        topic : 'travel',
        title : '20 top-rated tourist attractions in manhattan'
        },
        { 
        imgBgPath : require('../assets/images/img/blog-49.jpg'),
        topic : 'lifestyle',
        title : 'the best way to ride a motorcycle'
        },
        { 
        imgBgPath : require('../assets/images/img/blog-50.jpg'),
        topic : 'travel',
        title : '5 fun things to do at the beach'
        },
        { 
        imgBgPath : require('../assets/images/img/blog-51.jpg'),
        topic : 'recipes',
        title : 'amazingly fresh fruit and herbs drinks for summer'
        },
        ],

      postsCard : [
        {
          img : require('../assets/images/img/blog-54.jpg'),
          postTitle : 'How to make friends as a grown-up',
          textContent : 'Lorem ipsum dolor sit amet consectetur adipisicing elit. Repellat, in inventore? Impedit ex velit fuga dignissimos qui, dolorum quod eos ut eaque eveniet ea, aliquam porro, non deleniti? Rem, reprehenderit?',
          date : '12',
          month : 'jan',
          author : 'John Doe',
          topic : 'Lifestyle, Travel',
          comments : '12'
        },
        {
          img : require('../assets/images/img/blog-55 (1).jpg'),
          postTitle : 'Simple Ways to Have a Pretty Face',
          textContent : 'Lorem ipsum dolor sit amet consectetur adipisicing elit. Repellat, in inventore? Impedit ex velit fuga dignissimos qui, dolorum quod eos ut eaque eveniet ea, aliquam porro, non deleniti? Rem, reprehenderit?',
          date : '12',
          month : 'jan',
          author : 'John Doe',
          topic : 'Photography, Travel',
          comments : '12'
        },
        {
          img : require('../assets/images/img/blog-56 (1).jpg'),
          postTitle : 'Ranking the greatest players in basketball',
          textContent : 'Lorem ipsum dolor sit amet consectetur adipisicing elit. Repellat, in inventore? Impedit ex velit fuga dignissimos qui, dolorum quod eos ut eaque eveniet ea, aliquam porro, non deleniti? Rem, reprehenderit?',
          date : '12',
          month : 'jan',
          author : 'John Doe',
          topic : 'Sports, Business',
          comments : '12'
        },
        {
          img : require('../assets/images/img/blog-58 (1).jpg'),
          postTitle : 'Top Camper Trailer Towing Tips',
          textContent : 'Lorem ipsum dolor sit amet consectetur adipisicing elit. Repellat, in inventore? Impedit ex velit fuga dignissimos qui, dolorum quod eos ut eaque eveniet ea, aliquam porro, non deleniti? Rem, reprehenderit?',
          date : '12',
          month : 'jan',
          author : 'John Doe',
          topic : 'Travel, Lifestyle',
          comments : '12'
        },
      ],
  }
}
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped lang="scss">
@import "../style/variables.scss";

  .jumbotron_container {
    padding: 50px 0 20px 0;
    background-color: $jumbotronBg;
  }

  .pages_box {

    height: 100px;
    border-top : 1px solid $dateFont;
    display: flex;
    justify-content: flex-end;
    align-items: center;

    a {
      height: 40px;
      width: 30px;
      line-height: 40px;
      border: 2px solid $dateCalendar;
      text-decoration: none;
      text-align: center;
      display: inline-block;

        &:hover,
        &:active {
          background-color: $headerBg;
          color: $whiteColor;
        }
    }
  }

</style>
