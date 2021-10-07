<template>
    <main>
      <div class="container">
        <!-- Jumbotron section with topic-based content cards -->
            <div class="row">
              <CardJumbotron class="col-4 d-flex justify-content-between" 
              v-for="(element, index) in topicCard" :key="index" :topic="element"/>
          </div>

        <!-- Posts collection section -->
          <div class="row mb-5">
            <!-- Popular posts section -->
            <div class="col-4 posts_collection">
              <h6 class="h6_style">Popular posts</h6>
              <div v-for="(element, index) in popularPostsCollection" :key="index">
                <img :src="element.imgPost" alt="post image">
                <div class="caption_img_post">
                  <div>{{element.titlePost}}</div>
                  <div>{{element.datePost}}</div>
                </div>
              </div>
            </div>

            <!-- Recent posts section -->
            <div class="col-4 posts_collection">
                <h6 class="h6_style">Recent posts</h6>
                <div v-for="(element, index) in recentPostsCollection" :key="index">
                  <img :src="element.imgPost" alt="post image">
                  <div class="caption_img_post">
                    <div>{{element.titlePost}}</div>
                    <div>{{element.datePost}}</div>
                  </div>
              </div>
            </div>

            <!-- Featured posts section -->
            <div class="col-4">
              <h6 class="h6_style">Featured posts</h6>
              <div class="recipe_img mb-4">
                <img src="../assets/images/img/blog-66 (1).jpg" alt="recipe post image">
                <button class="bottom_left_topic btn btn-primary">Recipes</button>
                <h6 class="bottom_left_title">Tips to help you quickly prepare your lunch</h6>
              </div> 

              <h6 class="h6_style mb-3">Featured author</h6>
              <img class="avatar_img" src="../assets/images/img/avatar.jpg" alt="John Doe image">
              <div class="avatar_caption_box">
                <div class="fw-bold prova">John Doe</div>
                <div class="prova">Lorem ipsum dolor, sit amet consectetur adipisicing elit. Lorem ipsum dolor, sit amet consectetur adipisicing elit.</div>
              </div>
            </div>
          </div>
      </div>

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

          <CardPostTravel />


          <AsideSocialMedia class="col-2"/>
        </div>

      </div>

      
    </main>
</template>

<script>
import CardJumbotron from './CardJumbotron.vue';
import CardPost from './CardPost.vue';
import CardPostTravel from './CardPostTravel.vue'
import AsideSocialMedia from './AsideSocialMedia.vue';

export default {
  name: 'Main',
  props: {

  },
  components: {
    CardJumbotron,
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
      margin: 15px 10px 10px 0;
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

    .recipe_img {
        position: relative;
        margin-top: 20px;

        img {
            width: 350px;
            height: 150px;
            object-fit: cover;
            filter: brightness(50%);
        }
    }

    .bottom_left_topic {
        position: absolute;
        bottom: 40px;
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
    }

    .avatar_img {
      width: 90px;
      height: 90px;
      margin-right: 15px;
    }

    .avatar_caption_box {
      display: inline-block;
      width: 250px;
      height: 50px;
      font-size: 10px;
    }

    .topic_btn_wrap {
       background-color: $headerBg;
    }

    .topic_btn {
      display: inline-block;
    }
</style>
