<template>
  <header>
    <HeaderTop :menuHeaderTop="menuHeaderTop"/>
  </header>
</template>


<script>
import HeaderTop from "./HeaderTop.vue";

export default {
    name: "MainHeader",
    components: { HeaderTop },
    data() {
    return {
        menuHeaderTop: [
          'Sign In', 'About Us', 'Contact Us', 'Buy Now'
        ],
    }
  } 
}

</script>


<style scoped lang="scss">

</style>
