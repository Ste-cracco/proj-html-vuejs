<template>
    <div class="header_top flex">
      <div class="container">
        <div class="row">
          <menu class="flex">
            <ul class="menu flex">
              Everything about Lifestyle, Travel and Gadgets
              <li v-for="(item, i) in menuHeaderTop" :key="i">
                <a href="#" > 
                        {{ item }}
                </a>
              </li>
            </ul>                
            <div class="icone_social flex">
                    <font-awesome-icon icon="fa-brands fa-facebook-f" />
                    <font-awesome-icon icon="fa-brands fa-twitter" />
                    <font-awesome-icon icon="fa-brands fa-linkedin" />
            </div>
          </menu>  <!-- Fine Menu -->
        </div> <!-- Fine Row Menu -->
      </div> <!-- Fine Container Menu -->
    </div> <!-- Fine Header Top -->    
  </template>
  
  <script>
  export default {
    name: 'HeaderTop',
    props: {
      menuHeaderTop: Array,
    }
  }
  
  </script>
  
  <style scoped lang="scss">
  
    .header_top {
      background-color: var(--azzurro);
      min-height: 50px;
      align-items: center;

      .icone_social {
      margin-left: auto;
      color: white;
      gap: 30px;
      }
  
      ul {
        color: white;
        font-size: 0.9rem;
        gap: 30px;
  
        a {
        color: white;
        text-transform: uppercase;
        }
      } 
      
    }
  
  </style>
  