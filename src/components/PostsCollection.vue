<template>
  <div>
    <!-- Posts collection section -->
    <div class="container">
        <div class="row mb-5">
        <!-- Popular posts section -->
        <div class="col-4 posts_collection">
            <h6 class="h6_style">Popular posts</h6>
            <PopularPosts v-for="(element, index) in popularPostsCollection" :key="index" :popularPost="element"/>
        </div>
    
        <!-- Recent posts section -->
        <div class="col-4 posts_collection">
            <h6 class="h6_style">Recent posts</h6>
            <RecentPosts v-for="(element, index) in recentPostsCollection" :key="index" :recentPost="element"/>
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
  </div>
</template>

<script>
import PopularPosts from './PopularPosts.vue';
import RecentPosts from './RecentPosts.vue'

export default {
    name : 'PostsCollection',
    props : [''],
    components : {
        PopularPosts,
        RecentPosts
    },
    data : function () {
        return {
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
        }
    }
}
</script>

<style lang="scss">
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

</style>