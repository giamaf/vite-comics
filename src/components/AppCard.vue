<script>
export default {
    // Logica Javascript
    name: 'AppCard',

    props: {
        cards: Object
    },

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
    <div class="film-card">
        <img :src="cards.thumb" :alt="cards.series">
        <figcaption>{{ cards.series }}</figcaption>
    </div>
</template>
 
<style lang="scss" scoped>
/* Style */
.film-card {

    &:hover {
        cursor: pointer;
        filter: brightness(0.5);
    }

    figcaption {
        color: white;
        font-size: 0.7rem;
        padding: 5px 0;
    }
}

// img{
//     clip-path: inset(0px 32px 40px 32px);
// }
</style>