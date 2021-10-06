<template>
  <div>
    
    <CardJumbotron v-for="(element, index) in topicCard" :key="index" :topic="element"/>


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
      topicCard : [{

        imgBgPath : require('../assets/images/img/blog-46.jpg'),
        topic : 'photography',
        title : 'how to take better concert pictures in 30 seconds'
      }]
        
        

    
  }
}
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped lang="scss">
@import "../style/variables.scss";

</style>
