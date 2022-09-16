<template>
    <div class="container_content_bottom flex">
        <div class="container">
            <div class="row flex">
                <div class="col_1 ">
                    <PostSingolo v-for="(post,i) in posts" :key="i" :post = "post"/>
                    <div class="bordo_separatore"></div>
                    <div class="container_numero_pagine">
                        <div class="numero_pagine flex" >
                            <span class="pagina"> <font-awesome-icon icon="fa-solid fa-angle-left" /> </span>
                            <span class="pagina active"> 1 </span>
                            <span class="pagina"> 2 </span>
                            <span class="pagina"> 3 </span>
                            <span class="pagina"> <font-awesome-icon icon="fa-solid fa-angle-right" /> </span>
                        </div>
                    </div>
                </div>
                <div class="col_2">

                    <h5> Latest from Twitter</h5>
                    <div class="container_twitter_post flex">
                        <font-awesome-icon icon="fa-brands fa-twitter" />
                        <div class="testo_twitter_post">
                            <p> If you have any suggestions for the next updates, let us know. </p>
                            <a href="#">01:05 PM Sep 18th</a>
                        </div>
                    </div>
                    <div class="container_twitter_post flex">
                        <font-awesome-icon icon="fa-brands fa-twitter" />
                        <div class="testo_twitter_post">
                            <p> We have just updated Porto Admin. Check the changelog for more information. </p>
                            <a href="#">01:04 PM Sep 18th</a>
                        </div>
                    </div>

                    <h5>Photo from Instagram</h5>
                    <div class="container_instagram_photos grid">
                        <img src="../assets/images/IG_1.jpg" alt="">
                        <img src="../assets/images/IG_2.jpg" alt="">
                        <img src="../assets/images/IG_3.jpg" alt="">
                        <img src="../assets/images/IG_4.jpg" alt="">
                        <img src="../assets/images/IG_5.jpg" alt="">
                        <img src="../assets/images/IG_6.jpg" alt="">
                    </div>

                    <h5>Tags</h5>
                    <div class="container_tags flex">
                        <a class="tag" href="#">Design</a>
                        <a class="tag" href="#">Design</a>
                        <a class="tag" href="#">Design</a>
                        <a class="tag" href="#">Design</a>
                        <a class="tag" href="#">Design</a>
                        <a class="tag" href="#">Design</a>
                    </div>

                    <h5>Find Us on Facebook</h5>
                    <div class="container_facebook_link flex">
                        <blockquote> </blockquote>
                        <a href="#">Okler Themes</a>
                    </div>

                </div>
            </div>
        </div>
    </div>  
</template>
  
  
<script>
    
import PostSingolo from "./PostSingolo.vue";
 
  export default {
    name: "MainContentBottom",
    components: { PostSingolo },
    data() {
        return {
            posts: [
                {
                    image: require("../assets/images/blog-54.jpg"),
                    title: "How to Make Friends as a Grow-Up",
                    text: "Euismod atras vulputate iltricies etri elit. Class aptent taciti sociosqu ad litora torquent per conubia nostra, per inceptos himenaeos. Nulla nunc dui, tristique in semper vel, congue sed ligula. Nam dolor ligula, faucibus id sodales in, auctor fringilla libero. Pellentesque pellentesque tempor tellus eget hendrerit. Morbi id aliquam ligula. Aliquam id dui sem. Proin rhoncus consequat nisl, eu ornare mauris tincidunt vitae. [...]",
                    author: "John Doe",
                    tags: ["Lifestyle", "Travel"],
                    number_comments: "12 Comments",
                },
                {
                    image: require("../assets/images/blog-55 (1).jpg"),
                    title: "Simple Ways to Have a Pretty Face",
                    text: "Euismod atras vulputate iltricies etri elit. Class aptent taciti sociosqu ad litora torquent per conubia nostra, per inceptos himenaeos. Nulla nunc dui, tristique in semper vel, congue sed ligula. Nam dolor ligula, faucibus id sodales in, auctor fringilla libero. Pellentesque pellentesque tempor tellus eget hendrerit. Morbi id aliquam ligula. Aliquam id dui sem. Proin rhoncus consequat nisl, eu ornare mauris tincidunt vitae. [...]",
                    author: "John Doe",
                    tags: ["Lifestyle", "Travel"],
                    number_comments: "12 Comments",
                },
                {
                    image: require("../assets/images/blog-56 (1).jpg"),
                    title: "Ranking the greatest players in basketball",
                    text: "Euismod atras vulputate iltricies etri elit. Class aptent taciti sociosqu ad litora torquent per conubia nostra, per inceptos himenaeos. Nulla nunc dui, tristique in semper vel, congue sed ligula. Nam dolor ligula, faucibus id sodales in, auctor fringilla libero. Pellentesque pellentesque tempor tellus eget hendrerit. Morbi id aliquam ligula. Aliquam id dui sem. Proin rhoncus consequat nisl, eu ornare mauris tincidunt vitae. [...]",
                    author: "John Doe",
                    tags: ["Lifestyle", "Travel"],
                    number_comments: "12 Comments",
                },
                {
                    image: require("../assets/images/blog-58 (1).jpg"),
                    title: "Top Camper Trailer Towing Tips",
                    text: "Euismod atras vulputate iltricies etri elit. Class aptent taciti sociosqu ad litora torquent per conubia nostra, per inceptos himenaeos. Nulla nunc dui, tristique in semper vel, congue sed ligula. Nam dolor ligula, faucibus id sodales in, auctor fringilla libero. Pellentesque pellentesque tempor tellus eget hendrerit. Morbi id aliquam ligula. Aliquam id dui sem. Proin rhoncus consequat nisl, eu ornare mauris tincidunt vitae. [...]",
                    author: "John Doe",
                    tags: ["Lifestyle", "Travel"],
                    number_comments: "12 Comments",
                },
                {
                    image: require("../assets/images/blog-59.jpg"),
                    title: "10 Best Travel Tips After 5 Years Traveling The World",
                    text: "Euismod atras vulputate iltricies etri elit. Class aptent taciti sociosqu ad litora torquent per conubia nostra, per inceptos himenaeos. Nulla nunc dui, tristique in semper vel, congue sed ligula. Nam dolor ligula, faucibus id sodales in, auctor fringilla libero. Pellentesque pellentesque tempor tellus eget hendrerit. Morbi id aliquam ligula. Aliquam id dui sem. Proin rhoncus consequat nisl, eu ornare mauris tincidunt vitae. [...]",
                    author: "John Doe",
                    tags: ["Lifestyle", "Travel"],
                    number_comments: "12 Comments",
                },
            ]
        };
    }
}

</script>
  
  
<style scoped lang="scss">

    .container_content_bottom {

        @import '../style/col-1-main-content-bottom.scss';
        @import '../style/col-2-main-content-bottom.scss';
        
        
    }
    
  
</style>