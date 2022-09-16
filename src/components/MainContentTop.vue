<template>
    <div class="container_content_top">
        <div class="section_1">
            <div class="container">
                <div class="row">
                    <div class="container_card grid">
                        <PostPrincipali v-for="(card, i) in cards" :key="i" :card="card"/>
                    </div>
                </div>
            </div> <!-- Chiusura Container -->
        </div> <!-- Fine Section 1 -->
        
        <div class="section_2">
            <div class="container">
                <div class="row">
                    <div class="container_post grid">
                        <!-- Inizio Colonna 1 -->
                        <div class="col_1 flex_column">
                            <span class="categoria_post"> Popular posts </span>
                            <PostSecondari v-for="(post, i) in popularPosts" :key="i + 'a'" :post ="post"/>
                        </div>
                        <!-- Inizio Colonna 2 -->
                        <div class="col_2 flex_column">
                            <span class="categoria_post"> Recent Posts</span>
                            <PostSecondari v-for="(post, i) in recentPosts" :key="i + 'A'" :post ="post"/>
                        </div>
                        <!-- Inizio Colonna 3 -->
                        <div class="col_3">
                            <span class="categoria_post"> Featured Posts </span>
                            <PostPrincipali v-for="(card, i) in featuredPosts" :key="i + 'Aa'" :card ="card"/>
                            <span class="categoria_author"> Featured Author </span>
                            <!-- Card Featured Author -->
                            <article class="card_featured_author flex">
                                <img width="110px" src="../assets/images/avatar.jpg" alt="">
                                <div class="container_titolo_author">
                                    <h4 class="titolo_author"> John Doe </h4>
                                    <p> Lorem ipsum dolor sit amet consectetur adipisicing.
                                    Dolore mollitia dignissimos, recusandae vero inventore ipsam. </p>
                                </div>                                
                            </article>
                        </div>
                    </div> <!-- Chiusura Container Post -->
                </div> <!-- Chiusura Row -->
            </div> <!-- Chiusura Container -->
        </div> <!-- Fine Section 2 -->        
    </div>
</template>
  
  
<script>

import PostPrincipali from "./PostPrincipali.vue";
import PostSecondari from "./PostSecondari.vue";
 
  export default {
    name: "MainContentTop",
    components: { PostPrincipali, PostSecondari },
    data() {
        return {
            cards: [
                {
                    badge: "Photography",
                    title: "How To Take Better Concert Pictures in 30 Seconds",
                    image: require("../assets/images/blog-46.jpg")
                },
                {
                    badge: "Gadgets",
                    title: "Gadgets That Your Smartphone Even Smarter",
                    image: require("../assets/images/blog-47.jpg")
                },
                {
                    badge: "Travel",
                    title: "20 Top-Rated Tourist Attractions in Manhattan",
                    image: require("../assets/images/blog-48.jpg")
                },
                {
                    badge: "Lifestyle",
                    title: "The Best Way to Ride a Motocycle",
                    image: require("../assets/images/blog-49.jpg")
                },
                {
                    badge: "Travel",
                    title: "5 Fun Things to Do at the Beach ",
                    image: require("../assets/images/blog-50.jpg")
                },
                {
                    badge: "Recipes",
                    title: "Amazingly Fresh Fruit and Herb Drinks For Summer",
                    image: require("../assets/images/blog-46.jpg")
                },
            ],
            popularPosts: [
                {
                    title: "Simple Ways to Have a Pretty Face",
                    picture: require("../assets/images/blog-55.jpg"),
                    date: "January 12, 2019"
                },
                {
                    title: "Simple Ways to Have a Pretty Face",
                    picture: require("../assets/images/blog-56.jpg"),
                    date: "January 12, 2019"
                },
                {
                    title: "Simple Ways to Have a Pretty Face",
                    picture: require("../assets/images/blog-57.jpg"),
                    date: "January 12, 2019"
                },
                {
                    title: "Simple Ways to Have a Pretty Face",
                    picture: require("../assets/images/blog-58.jpg"),
                    date: "January 12, 2019"
                },
                {
                    title: "Simple Ways to Have a Pretty Face",
                    picture: require("../assets/images/blog-59.jpg"),
                    date: "January 12, 2019"
                },
            ],
            recentPosts: [
                {
                    title: "Simple Ways to Have a Pretty Face",
                    picture: require("../assets/images/blog-65.jpg"),
                    date: "January 12, 2019"
                },
                {
                    title: "Simple Ways to Have a Pretty Face",
                    picture: require("../assets/images/blog-66.jpg"),
                    date: "January 12, 2019"
                },
                {
                    title: "Simple Ways to Have a Pretty Face",
                    picture: require("../assets/images/blog-67.jpg"),
                    date: "January 12, 2019"
                },
                {
                    title: "Simple Ways to Have a Pretty Face",
                    picture: require("../assets/images/blog-68.jpg"),
                    date: "January 12, 2019"
                },
                {
                    title: "Simple Ways to Have a Pretty Face",
                    picture: require("../assets/images/blog-69.jpg"),
                    date: "January 12, 2019"
                },
            ],
            featuredPosts: [
                {
                    badge: "Photography",
                    title: "How To Take Better Concert Pictures in 30 Seconds",
                    image: require("../assets/images/blog-66.jpg")
                }
            ]
        };
    }
}

</script>
  
  
<style scoped lang="scss">
    .section_1 {
        background-color: #F7F7F7;
        padding: 50px 0;

        .container_card {
            grid-template-columns: 1fr 1fr 1fr;
            gap: 30px;
        }
    }

    .section_2 {
        padding: 50px 0;

        .container_post {
            grid-template-columns: 1fr 1fr 1fr;

            .categoria_post {
                font-size: var(--dimensione_titolo_secondario);
                text-transform: uppercase;
                font-weight: 700;
                color: #333;
                padding-bottom: 30px;
                display: block;
            }

            .categoria_author {
                font-size: var(--dimensione_titolo_secondario);
                text-transform: uppercase;
                font-weight: 700;
                color: #333;
                display: block;
                padding-top: 30px;
                padding-bottom: 15px;
            }

            .container_titolo_author {
                padding-left: 15px;

                .titolo_author {
                    padding-top: 5px;
                    padding-bottom: 10px;
                }

                p {
                    font-size: 0.8em;
                    color: var(--grigio_testo);
                    line-height: 25px;
                }            
            }
        }        
    }
  
</style>