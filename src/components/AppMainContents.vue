<script>
import AppCard from './AppCard.vue';
export default {
    name: 'AppMainContents',

    props: {
        mainCards: Array
    },

    components: {
        AppCard,
    }

};
</script>
 
<template>
    <main>
        <section>
            <div class="container">
                <div class="row">
                    <div v-for="(card, i) in mainCards" :key="i" class="col">
                        <AppCard :cards="card" />
                    </div>
                </div>
            </div>
            <button>
                <h5>Load More</h5>
            </button>
        </section>
    </main>
</template>
 
<style lang="scss" scoped>
main {
    background-color: rgba(0, 0, 0, 0.9);
    font-family: 'Open Sans';
    padding: 20px 0;
    text-align: center;

    .row {
        display: flex;
        flex-wrap: wrap;
        row-gap: 20px;
        column-gap: 15px;
        text-align: start;
    }

    .col {
        flex-basis: calc(100% / 5 - (60px / 5));
    }

    button {
        color: white;
        border: 1px solid transparent;
        background-color: rgb(12, 105, 247);
        // text-transform: uppercase;
        padding: 10px 35px;

        &:hover {
            cursor: pointer;
        }
    }
}
</style>
