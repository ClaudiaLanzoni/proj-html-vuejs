<template>
    <div>
        <div class="row">
            <div class="col-12 d-flex justify-content-between downer_footer_section">
                <div>
                    <img class="footer_logo" src="../assets/images/img/logo-footer.png" alt="Porto logo">
                    <div class="d-inline m-5">&copy; Copyright 2020. All rights reserved.</div>
                </div>

                <div>
                    <a class="m-3" href="#">FAQ's</a>
                    <a class="m-3" href="#">Sitemap</a>
                    <a class="m-3" href="#">Contact Us</a>
                </div>
            </div>
        </div>
    </div>
</template>

<script>
export default {
    name : 'FooterEnd',
    props : [''],
    data : function () {
    return {
   
    }
    }
}
</script>

<style scoped lang="scss">
@import "../style/variables.scss";

.footer_logo {
    width: 10%;
    filter: contrast(40%);
}

.downer_footer_section {
    height: 70px;
    line-height: 70px;
}

a {
    text-decoration: none;
    color: $downerFooterText;
}

</style>