<script>
  import AppNav from "./components/AppNav.vue"
  import AppContent from "./components/AppContent.vue"
  import AppFooter from "./components/AppFooter.vue"
  import AppSignUp from "./components/AppSignUp.vue"
  import AppBuy from "./components/AppBuy.vue"
 
  export default {
    components : {
      AppNav,
      AppContent,
      AppFooter,
      AppSignUp,
      AppBuy,
    }
  }

</script>

<template>

  <AppNav></AppNav>

  <AppContent></AppContent>

  <AppBuy></AppBuy>

  <AppFooter></AppFooter>

  <AppSignUp></AppSignUp>

</template>

<style scoped lang="scss">

</style>
