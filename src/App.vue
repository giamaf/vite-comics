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
 

<style>
/* CSS Reset */
* {
  margin: 0;
  padding: 0;
  box-sizing: border-box;
}

/* Generics */
body {
  font-family: 'Open Sans', sans-serif;
}

img {
  max-width: 100%;
  display: inline-block;
}

ul {
  list-style-type: none;
  text-transform: uppercase;
  gap: 20px;
}

a {
  text-decoration: none;
}


/* Utils */
.container {
  margin: 0 auto;
  max-width: 1200px;
}

.flex {
  display: flex;
  align-items: center;
}
</style>

