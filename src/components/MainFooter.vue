<template>
    <footer id="footer">
        <div class="container_footer_top">
            <div class="container">
                <div class="footer_ribbon">
                    <span> Get in Touch </span>
                </div>
                <div class="row grid">
                    <div class="container_about_the_blog">
                        <h6> About The Blog </h6>
                        <div class="container_contenuto">
                            <p>Lorem ipsum dolor sit amet consectetur, adipisicing elit. Fugit, debitis, sit amet consectetur.</p>
                            <p>Lorem ipsum dolor sit amet consectetur, adipisicing elit. Fugit, debitis, sit amet consectetur.</p>
                            <a href="#">View More <font-awesome-icon icon="fa-solid fa-angle-right" /> </a>
                        </div>
                    </div> 
                    <div class="container_recent_posts">
                        <h6> Recent Posts </h6>
                        <div class="container_contenuto flex" v-for="(post, i) in recentPosts" :key="i">                            
                            <img :src="post.image" alt="">
                            <div class="container_testo">
                                <p> {{ post.text }} </p>
                                <span> {{ post.date }} </span>
                            </div>
                        </div>    
                    </div>
                    <div class="container_recent_comments" >
                        <h6> Recent Comments </h6>
                        <div class="container_contenuto" v-for="(comment, i) in recentComments" :key=" i+'a'">
                            <span> <font-awesome-icon icon="fa-solid fa-angle-right" /> </span>
                            <span class="user"> {{ comment.user }} </span>
                            <span> commented on </span>
                            <span class="link_text"> {{ comment.linkText }} </span>
                            <span class="date"> {{ comment.date }} </span>
                        </div>                        
                    </div>           
                    <div class="container_categories" >
                        <h6> Categories </h6>
                        <div class="container_contenuto">
                            <ul class="flex_wrap">
                                <li v-for="(tag, i) in categories" :key=" i+'A'"> 
                                    {{ tag }} 
                                </li>
                            </ul>
                        </div>                        
                    </div> <!-- Chiusura Container Categories -->                  
                </div> <!-- Chiusura Row -->
            </div> <!-- Chiusura Container -->
        </div> <!-- Chiusura Container Footer Top -->  

        <div class="container_footer_bottom flex">
            <div class="container">
                <div class="row flex">
                    <div class="container_logo flex">
                        <img src="../assets/images/logo-footer.png" alt="">
                        <p> © Copyright 2020. All Rights Reserved </p>
                    </div>
                    <div class="container_menu flex">
                        <a href="#" v-for="(link, i) in menuFooter" :key="i+'Aa'"> 
                            <font-awesome-icon icon="fa-solid fa-angle-right" /> {{ link }}
                        </a>
                    </div>
                </div>
            </div>
        </div>      
    </footer>
</template>
  
  
<script>


 
  export default {
    name: "MainFooter",
    data() {
        return {
            recentPosts: [
                {
                    image: require('../assets/images/our-office-4-square.jpg'),
                    text: 'Lorem ipsum dolor sit amet consectetur, adipisicing elit',
                    date: '12:53 AM Dec 19th'
                },
                {
                    image: require('../assets/images/our-office-5-square.jpg'),
                    text: 'Lorem ipsum dolor sit amet consectetur, adipisicing elit',
                    date: '12:53 AM Dec 19th'
                },
            ],
            recentComments: [
                {
                    user: 'John Doe',
                    linkText: 'Lorem ipsum dolor sit amet',
                    date: '12:54 AM Dec 19th'
                },
                {
                    user: 'John Doe',
                    linkText: 'Lorem ipsum dolor sit amet',
                    date: '12:54 AM Dec 19th'
                }
            ],
            categories: [
                'Gadgets', 'Photography', 'Lifestyle', 'Fashion', 'Recipes', 'Travel', 'Business', 
                'Architecture', 'Reviews', 'Sport', 'Video', 'Technology', 'Design'
            ],
            menuFooter: ['FAQ\'s', 'Sitemap','Contact Us']
        }
    }
  }

</script>
  
  
<style scoped lang="scss">

    
    @import '../style/footerRibbon.scss';
    @import '../style/footerTop.scss';

    .container_footer_bottom {
        background-color: #1C2023;
        height: 150px;
        align-items: center;

        .row {
            justify-content: space-between;

            .container_logo img  {
                width: 85px;
                opacity: 0.6;
            }

            .container_logo p {
                padding-left: 50px;
                align-self: center;
                color: var(--grigio);
            }

            .container_menu {
                gap: 20px;

                a {
                    color: var(--grigio);
                }
            }
        } 
    }
  
</style>