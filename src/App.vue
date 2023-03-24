<script>
  import AppNav from "./components/AppNav.vue"
  import AppContent from "./components/AppContent.vue"
  import AppFooter from "./components/AppFooter.vue"
  import AppSignUp from "./components/AppSignUp.vue"

  export default {
    components : {
      AppNav,
      AppContent,
      AppFooter,
      AppSignUp,
    }
  }

</script>

<template>

  <AppNav></AppNav>

  <AppContent></AppContent>

  <AppFooter></AppFooter>

  <AppSignUp></AppSignUp>

</template>

<style scoped lang="scss">

</style>
