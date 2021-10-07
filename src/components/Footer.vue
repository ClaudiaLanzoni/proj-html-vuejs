<template>
    <div>
        <div class="footer_main_specifications_wrap">
            <div class="container">
                <FooterBlogReturn />
            </div>
        </div>

        <div class="footer_minor_specifications_wrap">
            <div class="container">
                <div class="row">
                    <div class="col-2">

                    </div>

                    <div class="col-2">

                    </div>
                </div>
            </div>
        </div>
    </div>
</template>

<script>
import FooterBlogReturn from './FooterBlogReturn.vue';

export default {
    name : 'Footer',
    props: {

    },
    components: {
        FooterBlogReturn,

  },
}
</script>

<style scoped lang="scss">
@import "../style/variables.scss";

</style>