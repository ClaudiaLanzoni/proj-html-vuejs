<template>
    <div class="post_container mb-5">
        <img class="img-fluid mb-3" :src="post.img" alt="post image">
        
        <!--Calendary page -->
        <div class="mt-2">

            <div>
                <div class="date_square text-center">{{post.date}}</div>
                <div class="month_square text-center">{{post.month}}</div>
            </div>

            <!-- Title and content section -->
            <div class="post_content_box">
                <h3 class="mb-3">{{post.postTitle}}</h3>

                <p>{{post.textContent}}</p>

                 <!-- Author, comments section -->
                <div class="author_box">
                    <span>&#128483; By</span> <a href="#">{{post.author}} </a>
                    <span>&#128448;</span> <a href="#"> {{post.topic}} </a>
                    <span>&#128490;</span> <a href="#"> {{post.comments}} Comments</a>

                    <button type="button" class="btn btn-light read_btn">Read more</button>
                </div>
            </div>

        </div>

        

    </div>
</template>

<script>


export default {
    name : 'CardPost',
    props : ['post'],
    components : {
 
    },
    data : function () {
        return {
        
    }
    }
}
</script>

<style lang="scss">
@import "../style/variables.scss";

    .date_square {
        width: 40px;
        height: 40px;
        line-height: 40px;
        background-color: $dateCalendar;
        margin-bottom: 8px;
        font-size: 13px;
        font-weight: bolder;
    }

    .month_square {
        width: 40px;
        height: 20px;
        line-height: 20px;
        background-color: $blackColor;
        color: $whiteColor;
        text-transform: uppercase;
        font-size: 10px;
    }

    .post_content_box {
        margin-left: 60px;
        margin-top: -70px;

        p {
            font-size: 13px;
            color: $postContentFont;
        }
    }

    .author_box {
        font-size: 12px;

        a {
            display: inline-block;
            margin-right: 15px;
            text-decoration: none;
        }
    }

    .read_btn {
        text-transform: uppercase;
        float: right;
        margin-top: -10px;
    }

</style>