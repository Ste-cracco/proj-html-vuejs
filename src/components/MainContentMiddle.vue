<template>
    <div class="container_content_middle flex">
        <div class="container">
            <div class="row">
                <div class="container_badge flex">
                    <font-awesome-icon icon="fa-solid fa-angle-left" class="icon" />
                    <div class="badge">
                        Gadgets
                    </div>
                    <div class="badge">
                        Photography
                    </div>
                    <div class="badge">
                        Lifestyle
                    </div>
                    <div class="badge">
                        Fashion
                    </div>
                    <div class="badge">
                        Recipes
                    </div>
                    <div class="badge">
                        Travel
                    </div>
                    <font-awesome-icon icon="fa-solid fa-angle-right" class="icon" />
                </div>
            </div>
        </div>
    </div>  
</template>
  
  
<script>
 
  export default {
    name: "MainContentMiddle",
}

</script>
  
  
<style scoped lang="scss">

    .container_content_middle {
        height: 150px;
        margin-bottom: 50px;
        background-color: var(--azzurro);
        align-items: center;

        .container_badge {
            justify-content: center;
            gap: 30px;
            color: white;
            text-transform: uppercase;

            .icon {
                align-self: center;
                color: var(--grigio_molto_scuro);
            }
            
            .badge {
                background-color: var(--grigio_molto_scuro);
                padding: 15px 45px;
                font-size: .9em;
                font-weight: 700;
            }     
            
            .badge:hover {
                background-color: #32383e;;
                cursor: pointer;
                
            }
        }
    }    
  
</style>