<script>
import AppHeader from './components/AppHeader.vue';
import AppMainContents from './components/AppMainContents.vue';
import AppAsideContents from './components/AppAsideContents.vue';
import AppFooterTop from './components/AppFooterTop.vue';
import AppFooterBottom from './components/AppFooterBottom.vue';
export default {
  // Logica Javascript
  name: 'DC Comics',

  components: {
    AppHeader,
    AppMainContents,
    AppAsideContents,
    AppFooterTop,
    AppFooterBottom,
  }

};

</script>
 
<!-- Template -->
<template>
  <AppHeader />
  <AppMainContents />
  <AppAsideContents />
  <footer>
    <AppFooterTop />
    <AppFooterBottom />
  </footer>
</template>
 

<style lang="scss">
@use './assets/scss/style.scss';
</style>

