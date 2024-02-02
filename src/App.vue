<script>
import AppHeader from './components/AppHeader.vue';
import AppMainContents from './components/AppMainContents.vue';
import AppAsideContents from './components/AppAsideContents.vue';
import AppFooterTop from './components/AppFooterTop.vue';
import AppFooterBottom from './components/AppFooterBottom.vue';

import { headerLinks, asideItems, footerTopList, footerBottomIcons } from './assets/data/index'
export default {
  // Logica Javascript
  name: 'DC Comics',

  components: {
    AppHeader,
    AppMainContents,
    AppAsideContents,
    AppFooterTop,
    AppFooterBottom,
  },

  data: () => ({
    headerLinks,
    asideItems,
    footerTopList,
    footerBottomIcons
  }),

};

</script>
 
<!-- Template -->
<template>
  <AppHeader :links="headerLinks" />
  <AppMainContents />
  <AppAsideContents :items="asideItems" />
  <footer>
    <AppFooterTop :footerTopList="footerTopList" />
    <AppFooterBottom :footerBottomIcons="footerBottomIcons" />
  </footer>
</template>
 

<style lang="scss">
@use './assets/scss/style.scss';
</style>

