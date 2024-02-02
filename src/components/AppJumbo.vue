<script>
export default {
    // Logica Javascript
    name: 'AppJumbo',

    computed: {
        createPath() {
            const url = new URL(`../assets/img/`, import.meta.url)
            return url.href
        }
    }
};
</script>
 
<template>
    <!-- Template -->
    <section class="jumbotron">

    </section>
</template>
 
<style lang="scss" scoped>
/* Style */
.jumbotron {
    background-image: url('../assets/img/jumbotron.jpg');
    background-size: cover;
    height: 400px;
}
</style>
