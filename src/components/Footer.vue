<template>
    <div>
        <div class="footer_main_specifications_wrap">
            <div class="container">
                <FooterBlogReturn />
            </div>
        </div>

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
    padding: 20px 0 20px 0;
    background-color: $upperFooterBg;
    color: $whiteColor;
}

.footer_minor_specifications_wrap {
    background-color: $downerFooterBg;
    color : $downerFooterText;
}   

</style>