<template>
    <main>
        <div class="section_1">
            <div class="container">
                <div class="row">
                    <div class="container_card grid">
                        <article class="card" v-for="(card, i) in cards" :key="i">
                            <span class="badge"> {{ card.badge }} </span>
                            <h3 class="titolo"> {{ card.title }} </h3>
                            <img :src="card.image" alt="">
                        </article>
                    </div>    
                </div>
            </div> <!-- Chiusura Container -->
        </div> <!-- Fine Section 1 -->
        <div class="section_2">
            <div class="container">
                <div class="row">
                    <div class="container_post grid">
                        <div class="col_1 flex_column">
                            <span> Popular posts </span>
                            <article class="post">
                                
                            </article>
                        </div>
                        <div class="col_2 flex_column">
                            <span>  Recent Posts</span>

                        </div>
                        <div class="col_3">
                            <span> Featured Posts </span>

                        </div>
                    </div>    
                </div>
            </div> <!-- Chiusura Container -->
        </div> <!-- Fine Section 2 -->
        
    </main>
</template>
  
  
<script>
 
  export default {
    name: 'MainContent',
    data() {
        return {
            cards: [
                {
                    badge: 'Photography',
                    title: 'How To Take Better Concert Pictures in 30 Seconds',
                    image: require('../assets/images/blog-46.jpg')
                },
                {
                    badge: 'Gadgets',
                    title: 'Gadgets That Your Smartphone Even Smarter',
                    image: require('../assets/images/blog-47.jpg')
                },
                {
                    badge: 'Travel',
                    title: '20 Top-Rated Tourist Attractions in Manhattan',
                    image: require('../assets/images/blog-48.jpg')
                },
                {
                    badge: 'Lifestyle',
                    title: 'The Best Way to Ride a Motocycle',
                    image: require('../assets/images/blog-49.jpg')
                },
                {
                    badge: 'Travel',
                    title: '5 Fun Things to Do at the Beach ',
                    image: require('../assets/images/blog-50.jpg')
                },
                {
                    badge: 'Recipes',
                    title: 'Amazingly Fresh Fruit and Herb Drinks For Summer',
                    image: require('../assets/images/blog-46.jpg')
                },
            ],
            popular_posts: [
                {       
                    title: '',
                    date: ''
                },
            ],
            recent_posts: [
                {
                    title: '',
                    date: ''
                }
            ]
        }
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

            .card {
                position: relative;

                .badge {
                    background-color: var(--azzurro);
                    padding: 5px;
                    color: white;
                    text-transform: uppercase;
                    font-size: 0.6em;
                    border-radius: 2px;
                    font-weight: 700;
                    position: absolute;
                    left: 22px;
                    bottom: 86px;
                }

                .titolo {
                    font-size: 1.2rem;
                    position: absolute;                    
                    color: white;
                    bottom: 25px;
                    left: 22px;
                    right: 22px;                  
                }
            }
        }
    }

    .section_2 {
        padding: 50px 0;

        .container_post {
            grid-template-columns: 1fr 1fr 1fr;
        }
    }
  
</style>