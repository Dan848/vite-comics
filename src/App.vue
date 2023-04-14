<template>
  <AppHeader />
  <AppMain />
  <MainBridge />
  <AppFooter />
</template>

<script>
import AppHeader from './components/AppHeader.vue';
import AppMain from './components/AppMain.vue';
import MainBridge from './components/MainBridge.vue';
import AppFooter from './components/AppFooter.vue';
export default {
components: {
  AppHeader,
  AppMain,
  MainBridge,
  AppFooter
}
}
</script> 

<style lang="scss" scoped></style>