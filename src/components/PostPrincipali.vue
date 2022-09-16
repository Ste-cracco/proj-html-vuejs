<template>    
    <article class="card">
        <img :src="card.image" alt="">
        <div class="container_titolo">
            <span class="badge"> {{ card.badge }} </span>
            <h3 class="titolo"> {{ card.title }} </h3>
        </div>
    </article>    
</template>
  
  <script>
  export default {
    name: 'PostPrincipali',
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
            color: var(--bianco);
            text-transform: uppercase;
            font-size: 0.6em;
            border-radius: 2px;
            font-weight: 700;
        }

        .titolo {
            font-size: 1.2rem;                   
            color: var(--bianco);
            padding-top: 10px;                 
        }
    
    img:hover {
        -webkit-filter: brightness(50%);
        cursor: pointer;
    }
    }

  </style>
  