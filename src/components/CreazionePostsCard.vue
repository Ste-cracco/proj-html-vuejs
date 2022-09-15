<template>    
    <article class="post flex">
        <img width="50px" :src="post.picture" alt="">
        <div class="titolo_post">
            <h4> {{ post.title }} </h4>
            <span> {{ post.date }} </span>
        </div>                                
    </article>   
</template>
  
<script>
  export default {
    name: 'CreazioneCard',
    props: {
        post: Object,
    }
  }
  
</script>
  
<style scoped lang="scss">
    .post {
        padding: 15px 0;
        
        .titolo_post {
            padding-left: 15px;

            span {
                font-size: 0.8em;
                color: #B7B7B7;
            }
        }
    }
</style>