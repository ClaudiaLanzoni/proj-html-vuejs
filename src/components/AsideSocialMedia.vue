<template>
    <div>
        <div>

            <!--Twitter section-->
            <div class="mb-5">
                <h6 class="h6_style">Latest from Twitter</h6>
                <div class="mb-4">
                    <div>If you have any suggestions for the next updates, let us know.</div>
                    <div><span class="blue_text">01:05 PM Sep 18th</span></div>
                </div>


                <div>
                    <div>We have just updated Porto Admin. Check the changelog for more information.</div>
                    <div><span class="blue_text">01:04 PM Sep 18th</span></div>
                </div>
            </div>

            <!-- Instagram section -->
            <div class="mb-5">
                <h6 class="h6_style">Photos from Instagram</h6>

                <div class="multiple_img_container">
                    <span class="multiple_img_container"
                    v-for="(element, index) in imgOfMultipleImgs" :key="index">
                    
                        <img class="img-fluid" :src="element.imgPath" alt="instagram image">
                        
                    </span>
                </div>
            </div>

            <!--Tags section-->
            <div class="mb-5">
                <h6 class="h6_style">Tags</h6>
                <div class="tags_container"
                    v-for="(element, index) in tagsList" :key="index">
                    <div class="tag_btn fw-bold text-center">{{element.tagName}}</div>
                </div>
            </div>

            <!--Facebook section-->
            <div class="mb-5">
                <h6 class="h6_style">Find us on facebook</h6>

                <!-- vertical lign before theme -->
                <div class="vertical_lign"></div>

                <p class="d-inline"><span class="blue_text">Okler Themes</span></p>
            </div>
        </div>
      
    </div>
</template>

<script>
export default {
    name : 'AsideSocialMedia',
    props : [''],
    data : function () {
        return {
        
        imgOfMultipleImgs : [
        {
        imgPath : require('../assets/images/img/29739607_2020680068220520_4509928046932787200_n.jpg')
        },
        {
        imgPath : require('../assets/images/img/30087804_253872848488989_8792603541668626432_n.jpg')
        },
        {
        imgPath : require('../assets/images/img/29415620_196477127626244_3250318472361541632_n.jpg')
        },
        {
        imgPath : require('../assets/images/img/30078414_1274410412703843_8290935809419247616_n.jpg')
        },
        {
        imgPath : require('../assets/images/img/30077195_2066750973610181_3733150062893596672_n.jpg')
        },
        {
        imgPath : require('../assets/images/img/29415304_166583630713703_1032667922171953152_n.jpg')
        },
        ],

        tagsList : [
        {
            tagName : 'design'
        },
        {
            tagName : 'brands'
        },
        {
            tagName : 'video'
        },
        {
            tagName : 'business'
        },
        {
            tagName : 'travel'
        },
        ],

    }
    }
}
</script>

<style scoped lang="scss">
@import "../style/variables.scss";


    h6  {
        margin-bottom: 20px;
    }

    .multiple_img_container {
        
        img {
            width: 100px;
            height: 100px;
            display: inline-block;
        }

    }

    .tags_container {
        display: inline-block;
    }

    .vertical_lign {
        height: 30px;
        width: 4px;
        background-color: rgb(190, 181, 181);
        display: inline-block;
        margin-right: 20px;
    }

</style>