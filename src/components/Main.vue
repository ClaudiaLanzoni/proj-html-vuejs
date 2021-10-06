<template>
    <main>
      <div class="container">
            <div class="row">
              <CardJumbotron class="col-4 d-flex justify-content-between" 
              v-for="(element, index) in topicCard" :key="index" :topic="element"/>
          </div>

          <div class="row">
            <div class="col-4 posts_collection">
              <h6>Popular posts</h6>
              <div v-for="(element, index) in popularPostsCollection" :key="index">
                <img :src="element.imgPost" alt="post image">
                <div class="caption_img_post">
                  <div>{{element.titlePost}}</div>
                  <div>{{element.datePost}}</div>
                </div>
              </div>
            </div>

            <div class="col-4 posts_collection">
                <h6>Recent posts</h6>
                <div v-for="(element, index) in recentPostsCollection" :key="index">
                  <img :src="element.imgPost" alt="post image">
                  <div class="caption_img_post">
                    <div>{{element.titlePost}}</div>
                    <div>{{element.datePost}}</div>
                  </div>
              </div>
            </div>

            <div class="col-4">
                <div>
                  <h6>Featured posts</h6>
                  <img src="" alt="">
                  <p></p>
                  <p></p>
                </div>
            </div>
          </div>
      </div>

      
    </main>
</template>

<script>
import CardJumbotron from './CardJumbotron.vue';

export default {
  name: 'Main',
  props: {

  },
  components: {
    CardJumbotron,
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

      popularPostsCollection : [
        {
          imgPost : require('../assets/images/img/blog-55.jpg'),
          titlePost : 'Simple ways to have a pretty face',
          datePost : 'January 12, 2019'
        },
        {
          imgPost : require('../assets/images/img/blog-56.jpg'),
          titlePost : 'Ranking the greatest players in basketball',
          datePost : 'January 12, 2019'
        },
        {
          imgPost : require('../assets/images/img/blog-57.jpg'),
          titlePost : '4 ways to look Cool in glasses',
          datePost : 'January 12, 2019'
        },
        {
          imgPost : require('../assets/images/img/blog-58.jpg'),
          titlePost : 'Top Camper Trailer Towing Tips',
          datePost : 'January 12, 2019'
        },
        {
          imgPost : require('../assets/images/img/blog-59.jpg'),
          titlePost : '5 lovely walks in New York',
          datePost : 'January 12, 2019'
        }
      ],

      recentPostsCollection : [
        {
          imgPost : require('../assets/images/img/blog-65.jpg'),
          titlePost : 'Main Reasons To Stop Texting And Driving',
          datePost : 'January 12, 2019'
        },
        {
          imgPost : require('../assets/images/img/blog-66.jpg'),
          titlePost : 'Tips to help you quickly prepare your lunch',
          datePost : 'January 12, 2019'
        },
        {
          imgPost : require('../assets/images/img/blog-67.jpg'),
          titlePost : 'Why should I buy a smartwatch?',
          datePost : 'January 12, 2019'
        },
        {
          imgPost : require('../assets/images/img/blog-68.jpg'),
          titlePost : 'The best augmented reality smartglasses',
          datePost : 'January 12, 2019'
        },
        {
          imgPost : require('../assets/images/img/blog-69.jpg'),
          titlePost : '12 Healthiest Food To Eat for Breakfast',
          datePost : 'January 12, 2019'
        }
      ]
    
  }
}
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped lang="scss">
@import "../style/variables.scss";

  .posts_collection {
    
    img {
      width: 50px;
      height: 50px;
      margin: 15px 10px 20px 0;
    }

    p {

      font-size: 12px;
    }

    div {
      font-size: 10px;
    }
  }

    .caption_img_post {
      display: inline-block;
    }
</style>
