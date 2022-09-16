<template>    
    <article class="flex_wrap" >
        <img :src="post.image" alt="">
        <div class="calendario flex_column">
            <span class="giorno"> 12 </span>
            <span class="mese"> Jan </span>
        </div>
        <div class="container_testo flex_column">
            <h3> {{ post.title }} </h3>
            <p> {{ post.text }} </p>
            <div class="tags flex">
                <div class="tag">
                    <font-awesome-icon icon="fa-regular fa-user" />
                    <a href="#"> {{ 'By '+ post.author }} </a>
                </div>
                <div class="tag">
                    <font-awesome-icon icon="fa-regular fa-folder" />
                    <a href="#"> {{ post.tags[0] }} {{ post.tags[1] }} </a>
                </div>
                <div class="tag last_tag">
                    <font-awesome-icon icon="fa-regular fa-comments" />
                    <a href="#"> {{ post.number_comments }} </a>
                </div>
                <div class="read_more">
                    <span> read more</span>
                </div>
            </div>
        </div>
    </article>
</template>
  
<script>
  export default {
    name: 'PostSingolo',
    props: {
        post: Object,
    }
  }
  
</script>
  
<style scoped lang="scss">

    img {
        aspect-ratio: 16/6;
        object-fit: cover;
        width: 100%;
    }

    .calendario {
        padding-top: 20px;        

        span {
            display: block;
        }
        
        .giorno {
            background-color: #F7F7F7;                   
            font-size: .9em;
            width: 45px;
            padding: 20px 0;
            text-align: center;
            font-weight: 800;
        }

        .mese {
            background-color: black;
            color: var(--bianco);
            text-transform: uppercase;
            font-size: .8em;
            width: 45px;
            padding: 3px 0;
            text-align: center;
        }
    }

    .container_testo {
        max-width: 95%;
        gap: 20px;
        padding: 20px;
        padding-bottom: 70px;

        h3 {
            font-size: 1.8rem;
            font-weight: 700;
        }

        p {
            color: var(--grigio_testo);
            line-height: 30px;
        }

        a {
            color: var(--azzurro);
            padding-left: 2px;
            padding-right: 16px;
        }

        .tags {            

            .read_more {
                text-transform: uppercase;
                border: 1px solid var(--grigio_chiaro);
                margin-left: auto;

                span {
                    font-size: 0.8em;
                    padding: 4px 7px;
                    display: block;
                    color: #888;
                }
            }
        }
    }
    
</style>