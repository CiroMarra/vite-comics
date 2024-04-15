<script>
import AppHeader from './components/AppHeader.vue';
import AppMain from './components/AppMain.vue';
import AppFooter from './components/AppFooter.vue';
import AppProductsList from './components/AppProductsList.vue';
export default {
  components: {
    AppHeader,
    AppMain,
    AppFooter,
    AppProductsList
  }
}
</script>

<template>
  <header>
   <AppHeader></AppHeader>
  </header>
  <main>
  <AppProductsList></AppProductsList>
   <AppMain></AppMain>
  </main>
  <footer>
    <AppFooter></AppFooter>
  </footer>
</template>

<style lang="scss">
@use './style/generic';
</style>