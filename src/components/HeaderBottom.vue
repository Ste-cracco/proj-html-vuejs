<template>
    <div class="header_bottom flex">
        <div class="container">
            <div class="row">
                <menu class="flex">
                    <ul class="menu flex">
                        <li v-for="(item, i) in menuHeaderBottom" :key="i">
                            <a href="#" >
                                {{ item }}
                            </a>
                        </li>
                    </ul>
                    <div class="container_search">
                        <font-awesome-icon icon="fa-solid fa-magnifying-glass" />
                    </div>
                </menu>
            </div> <!-- Fine Row Menu -->  
        </div> <!-- Fine Container Menu -->
    </div> <!-- Fine Header Top -->    
</template>
  

  <script>

  export default {
    name: 'HeaderFooter',
    props: {
        menuHeaderBottom: Array,
    }
  }
  
  </script>

  
  <style scoped lang="scss">

    .header_bottom {
        background-color: white;
        min-height: 65px;
        align-items: center;
        border-top: 1px solid lightgray;
        border-bottom: 1px solid lightgray;

        .container_search {
            margin-left: auto;
            color: #444;
        }

        ul {
            font-size: 1rem;
            gap: 50px;

            a {
                color: #444;
                text-transform: uppercase;
                font-weight: 700;
            }
            
        }     
    
    }

  </style>
  