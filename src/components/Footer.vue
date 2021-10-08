<template>
    <div>
        <!-- Upper footer section with major blog specifications -->
        <div class="footer_main_specifications_wrap">
            <div class="container">

                <!-- Get in touch box -->
                <div class="get_in_touch_box">
                    <div>Get in Touch</div>
                </div>
                

                <FooterBlogReturn />
            </div>
        </div>

        <!--Downer footer section with minor blog specifications-->
        <div class="footer_minor_specifications_wrap">
            <div class="container">

                <FooterEnd />
            
            </div>
        </div>
    </div>
</template>

<script>
import FooterBlogReturn from './FooterBlogReturn.vue';
import FooterEnd from './FooterEnd.vue';

export default {
    name : 'Footer',
    props: {

    },
    components: {
        FooterBlogReturn,
        FooterEnd
  },
}
</script>

<style scoped lang="scss">
@import "../style/variables.scss";

.footer_main_specifications_wrap {
    background-color: $upperFooterBg;
    padding: 20px 0 20px 0;
    color: $whiteColor;
}

.footer_minor_specifications_wrap {
    
    background-color: $downerFooterBg;
    color : $downerFooterText;
}   

.get_in_touch_box {
    width: 120px;
    height: 40px;
    line-height: 40px;
    background-color: $headerBg;
    font-size: 13px;
    text-align: center;
    margin-top: -35px;
    font-family: $getInTouchBoxFont;
}

</style>