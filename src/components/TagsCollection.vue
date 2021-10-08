<template>
    <div>      
        <div class="topic_link_wrap mb-5">
            <div class="container">
                <div class="row">
                    <div class="col-12 d-flex justify-content-between">
                      <a v-for="(element, index) in linksTopicsSlider" :key="index"
                      href="#">{{element.topicName}}</a>
                    </div>
                </div>
            </div>
        </div>
    </div>
</template>

<script>
export default {
    name : 'TagsCollection',
    props : ['topicTag'],
    data : function () {
        return {

        linksTopicsSlider : [

        {
          topicName : 'Gadgets'
        },
        {
          topicName : 'Photography'
        },
        {
          topicName : 'Lifestyle'
        },
        {
          topicName : 'Fashion'
        },
        {
          topicName : 'Recipes'
        },
        {
          topicName : 'Travel'
        }

      ],
        }
    }
}
</script>

<style scoped lang="scss">
@import "../style/variables.scss";

  .topic_link_wrap {
    background-color: $headerBg;
    padding: 40px;

      a {
        border-radius: 0%;
        font-size: 11px;
        text-transform: uppercase;
        font-weight: bolder;
        padding: 12px 50px;
        text-decoration: none;
        color: $whiteColor;
        background-color: $linkSlideBg;
    }
}

</style>