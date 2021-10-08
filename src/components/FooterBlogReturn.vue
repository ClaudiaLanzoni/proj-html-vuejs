<template>
  <div class="footer_return_wrap">
      <div class="row">

        <!-- About section -->
        <div class="col-3">
            <h6 class="h6_style">About the blog</h6>

            <p>Lorem ipsum dolor sit amet consectetur adipisicing elit. Doloremque incidunt error blanditiis.</p> 
                
            <p>Optio nemo reiciendis, molestiae tempore quo exercitationem mollitia commodi?</p>

            <h6 class="h6_style">View more</h6>
        </div>

        <!-- Recent posts section -->
        <div class="col-4">
            <h6 class="h6_style">Recent posts</h6>

            <img class="my_br mb-3" src="../assets/images/img/our-office-4-square.jpg" alt="office image">

            <div class="posts_wrap">
                <div>Lorem ipsum dolor sit amet consectetur, adipisicing elit.</div>
                <div>12:53 AM Dec 19th</div>
            </div>

            <img class="my_br" src="../assets/images/img/our-office-5-square.jpg" alt="office image">

            <div class="posts_wrap">
                <div>Lorem ipsum dolor sit amet consectetur, adipisicing elit.</div>
                <div>12:53 AM Dec 19th</div>
            </div>
        </div>

        <!-- Recent comments section -->
        <div class="col-2">

            <h6 class="h6_style">Recent comments</h6>

            <div class="mb-3">
                <div><span class="fw-bold">John Doe</span> commented on <span class="fw-bold">lorem ipsum dolor sit amet</span> </div>
                <div>12:55 AM Dec 19th</div>
            </div>

            <div>
                <div><span class="fw-bold">John Doe</span> commented on <span class="fw-bold">lorem ipsum dolor sit amet</span> </div>
                <div>12:55 AM Dec 19th</div>
            </div>
        </div>

        <!-- Categories section -->
        <div class="col-3">
            <h6 class="h6_style">Categories</h6>

            <div class="tags_container"
                v-for="(element, index) in categoriesList" :key="index">
                <div class="tag_btn cat_tag fw-bold text-center">{{element.categoryName}}</div>
            </div>


        </div>
    </div>
  </div>
</template>

<script>
export default {
    name : 'FooterBlogReturn',
    props : [''],
    data : function () {
    return {
        categoriesList : [
        {
            categoryName : 'gadgets'
        },
        {
            categoryName : 'photography'
        },
        {
            categoryName : 'lifestyle'
        },
        {
            categoryName : 'fashion'
        },
        {
            categoryName : 'recipes'
        },
        {
            categoryName : 'travel'
        },
        {
            categoryName : 'business'
        },
        {
            categoryName : 'architecture'
        },
        {
            categoryName : 'reviews'
        },
        {
            categoryName : 'sports'
        },
        {
            categoryName : 'videos'
        },
        {
            categoryName : 'technology'
        },
        {
            categoryName : 'design'
        },
        ]
    }
}
}
</script>

<style scoped lang="scss">
@import "../style/variables.scss";

.footer_return_wrap {
    font-size: 10px;
}

 .my_br {
    border-radius: 50%;
    width: 50px;
    height: 50px;
 }

 .posts_wrap {
    display: inline-block;
    margin-left: 10px;

 }

 .tags_container {
    display: inline-block;
 }

 .cat_tag {
    margin-bottom: 5px;
 }

</style>