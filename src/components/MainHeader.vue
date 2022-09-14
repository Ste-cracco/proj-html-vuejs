<template>
  <header>
    <HeaderTop :menuHeaderTop="menuHeaderTop"/>
    <HeaderMiddle/>
    <HeaderBottom :menuHeaderBottom="menuHeaderBottom"/>
    
  </header>
</template>


<script>
import HeaderTop from "./HeaderTop.vue";
import HeaderMiddle from "./HeaderMiddle.vue";
import HeaderBottom from "./HeaderBottom.vue";

export default {
    name: "MainHeader",
    components: { HeaderTop, HeaderMiddle, HeaderBottom },
    data() {
    return {
        menuHeaderTop: [
          'Sign In', 'About Us', 'Contact Us', 'Buy Now'
        ],
        menuHeaderBottom: [
          'Home', 'Elements', 'Features', 'Pages', 'Portfolio', 'Blog', 'Shop'
        ],
    }
  } 
}

</script>


<style scoped lang="scss">

</style>
