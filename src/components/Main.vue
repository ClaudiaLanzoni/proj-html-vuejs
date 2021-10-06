<template>
  <div>
    <main>
      <div class="container">
            <div class="row">
              
                  
              <CardJumbotron class="col-4 d-flex justify-content-between" 
              v-for="(element, index) in topicCard" :key="index" :topic="element"/>
                
          
          </div>
      </div>
    </main>
   


  </div>
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
        ]
        
        

    
  }
}
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped lang="scss">
@import "../style/variables.scss";


</style>
