<template>
  <AppHeader />
  <AppMain />
  <MainBridge />
</template>

<script>
import AppHeader from './components/AppHeader.vue';
import AppMain from './components/AppMain.vue';
import MainBridge from './components/MainBridge.vue';
export default {
components: {
  AppHeader,
  AppMain,
  MainBridge
}
}
</script> 

<style lang="scss" scoped></style>