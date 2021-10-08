<template>
    <div>
        <div class="small_container_img mb-3">
            <img v-for="(element, index) in imgCollection" :key="index"  class="img-fluid" :src="element.img" alt="blog small image">   
        </div>

        <div class="mt-4">
            <div v-for="(element, index) in content" :key="index">
                <div>
                    <div class="date_square text-center">{{element.date}}</div>
                    <div class="month_square text-center">{{element.month}}</div>
                </div>
                <div class="post_content_box mb-5">
                    <h3  class="mb-3">{{element.postTitle}}</h3>

                    <p>{{element.textContent}}</p>

                    <div class="author_box">
                    <span>&#128483; By</span> <a href="#">{{element.author}} </a>
                    <span>&#128448;</span> <a href="#"> {{element.topic}} </a>
                    <span>&#128490;</span> <a href="#"> {{element.comments}} Comments</a>

                    <button type="button" class="btn btn-light read_btn">Read more</button>
                </div>

            </div>
            </div>
        </div>
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

      content : [
        {
        textContent : 'Lorem ipsum dolor sit amet consectetur adipisicing elit. Repellat, in inventore? Impedit ex velit fuga dignissimos qui, dolorum quod eos ut eaque eveniet ea, aliquam porro, non deleniti? Rem, reprehenderit?',
        postTitle : '10 Best Travel Tips After 5 Years Travelling The World',
        date : '8',
        month : 'jan',
        author : 'John Doe',
        topic : 'Travel, Lifestyle',
        comments : '12'
        }
      ],
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