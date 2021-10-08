<template>
    <main>
      <div class="jumbotron_container mb-5">
        <div class="container">
        <!-- Jumbotron section with topic-based content cards -->
            <div class="row">
              <CardJumbotron class="col-4 d-flex justify-content-between" 
              v-for="(element, index) in topicCard" :key="index" :topic="element"/>
            </div>
        </div>
      </div>

      <PostsCollection />

      <!-- Blog's topics button section-->
      <div class="topic_btn_wrap mb-5">
          <div class="container">
            <div class="row">
              <div class="col-12">
                <div class="topic_btn" 
                v-for="(element, index) in buttonsTopicsSlider" :key="index">
                  
                <button type="button" class="btn btn-dark m-5">{{element.topicName}}</button>

              </div>
            </div>
          </div>
        </div>
      </div>
        
      <div class="container">
        <div class="row">
          <!-- Large posts section with content cards -->
          <CardPost class="col-8"
          v-for="(element, index) in postsCard" :key="index" :post="element"/>

          <CardPostTravel 
          v-for="(element, index) in imgCollection" :key="index" :smallimg="element"/>

          <AsideSocialMedia class="col-2"/>
        </div>

      </div>

      
    </main>
</template>

<script>
import CardJumbotron from './CardJumbotron.vue';
import PostsCollection from './PostsCollection.vue';
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

      buttonsTopicsSlider : [
        {
          topicName : 'Gadgets'
        },
        {
          topicName : 'Photography'
        },
        {
          topicName : 'Lifestyle'
        },
        {
          topicName : 'Fashion'
        },
        {
          topicName : 'Recipes'
        },
        {
          topicName : 'Travel'
        }

      ],

      postsCard : [
        {
          img : require('../assets/images/img/blog-54.jpg'),
          postTitle : 'How to make friends as a grown-up'
        },
        {
          img : require('../assets/images/img/blog-55 (1).jpg'),
          postTitle : 'Simple Ways to Have a Pretty Face'
        },
        {
          img : require('../assets/images/img/blog-56 (1).jpg'),
          postTitle : 'Ranking the greatest players in basketball'
        },
        {
          img : require('../assets/images/img/blog-58 (1).jpg'),
          postTitle : 'Top Camper Trailer Towing Tips'
        },
        {
          img : require('../assets/images/img/blog-58 (1).jpg'),
          postTitle : '10 Best Travel Tips After 5 Years Travelling The World'
        }
      ],

      imgCollection : [
      {
          img : require('../assets/images/img/blog-29.jpg'),
      },
      {
          img : require('../assets/images/img/blog-16.jpg'),
      },
      {
          img : require('../assets/images/img/blog-20.jpg'),
      },
      {
          img : require('../assets/images/img/blog-23.jpg'),
      },
      {
          img : require('../assets/images/img/blog-29.jpg'),
      },
      {
          img : require('../assets/images/img/blog-40.jpg'),
      },
      ]
  }
}
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped lang="scss">
@import "../style/variables.scss";


    .topic_btn_wrap {
       background-color: $headerBg;
    }

    .topic_btn {
      display: inline-block;
    }

    .jumbotron_container {
      padding: 50px 0 20px 0;
      background-color: $jumbotronBg;
    }
</style>
