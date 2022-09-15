<template>    
    <article class="card">
        <div class="container_titolo">
            <span class="badge"> {{ card.badge }} </span>
            <h3 class="titolo"> {{ card.title }} </h3>
        </div>
        <img :src="card.image" alt="">
    </article>    
</template>
  
  <script>
  export default {
    name: 'CreazioneCard',
    props: {
        card: Object,
    }
  }
  
  </script>
  
  <style scoped lang="scss">

    .card {
        position: relative;

        .container_titolo {
            position: absolute;
            bottom: 20px;
            left: 20px;
        }

        .badge {
            background-color: var(--azzurro);
            padding: 5px;
            color: white;
            text-transform: uppercase;
            font-size: 0.6em;
            border-radius: 2px;
            font-weight: 700;
        }

        .titolo {
            font-size: 1.2rem;                   
            color: white;
            padding-top: 10px;                 
        }
    }

  </style>
  