<template>
  <div>
      <div class="row">

        <!-- About section -->
        <div class="col-4">
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


        <div class="col-3">

        </div>

        <div class="col-2">

        </div>
    </div>
  </div>
</template>

<script>
export default {

}
</script>

<style scoped lang="scss">
@import "../style/variables.scss";

 .my_br {
    border-radius: 50%;
    width: 50px;
    height: 50px;
 }

 .posts_wrap {
    display: inline-block;
    margin-left: 10px;
    div {
        font-size: 12px;
    }
 }

</style>