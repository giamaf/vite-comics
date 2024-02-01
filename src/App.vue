<script>
import AppHeader from './components/AppHeader.vue';
export default {
  // Logica Javascript
  name: 'DC Comics',


  components: {
    AppHeader
  }

};

</script>
 
<!-- Template -->
<template>
  <div class="container">
    <AppHeader />
  </div>
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
  font-family: 'Open Sans Variable', 'Open Sans Condensed';
}

img {
  max-width: 100%;
  display: inline-block;
}

ul {
  list-style-type: none;
}

a {
  text-decoration: none;
  color: black;
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

