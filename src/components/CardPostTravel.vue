<template>
    <div>
        <div class="small_container_img mb-3">
            <img v-for="(element, index) in imgCollection" :key="index"  class="img-fluid" :src="element.img" alt="blog small image">   
        </div>

        <h3 v-for="(element, index) in titleName" :key="index" class="mb-3">{{element.postTitle}}</h3>

        <p v-for="(element, index) in content" :key="index" class="mb-5">{{element.textContent}}</p>
    </div>
        
</template>

<script>
export default {
    name : 'CardPostTravel',
    props : ['smallimg'],
    data : function () {
        return {

        imgCollection : [
      {
          img : require('../assets/images/img/blog-13.jpg'),
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
      ],

      titleName : [
        {
        postTitle : '10 Best Travel Tips After 5 Years Travelling The World'
        }
      ],

      content : [
        {
        textContent : 'Lorem ipsum dolor sit amet consectetur adipisicing elit. Repellat, in inventore? Impedit ex velit fuga dignissimos qui, dolorum quod eos ut eaque eveniet ea, aliquam porro, non deleniti? Rem, reprehenderit?'
        }
      ]
    }
    }
}
</script>

<style scoped lang="scss">
@import "../style/variables.scss";



.small_container_img {
    width: 750px;
    height: 500px;

    img {
    width: 250px;
    height: 250px;
    display: inline-block;

}
}



</style>