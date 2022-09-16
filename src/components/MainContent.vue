<template>
    <main>
        <MainContentTop/>
        <MainContentMiddle/>
        <MainContentBottom/>
    </main>
</template>
  
  
<script>
import MainContentTop from "./MainContentTop.vue";
import MainContentMiddle from "./MainContentMiddle.vue";
import MainContentBottom from "./MainContentBottom.vue";

 
  export default {
    name: "MainContent",
    components: { MainContentTop, MainContentMiddle, MainContentBottom }
}

</script>
  
  
<style scoped lang="scss">
  
</style>