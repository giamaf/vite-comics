<script>
export default {
    name: 'AppAsideContents',
    data: () => ({}),

    props: {
        items: Array
    },

    computed: {
        createPath() {
            const url = new URL(`../assets/img/`, import.meta.url)

            return url.href
        }
    }

}
</script>
 
<template>
    <aside>
        <div class="container">
            <ul class="flex">
                <li v-for="(item, i) in items" :key="i" class="flex">
                    <a href="#"><img :src="`${createPath}/${item.image}`" :alt="item.label"></a>
                    <label>{{ item.label }}</label>
                </li>
            </ul>
        </div>
    </aside>
</template>
 
<style lang="scss" scoped>
aside {
    background-color: rgb(12, 105, 247);
    font-size: 0.5rem;
    position: relative;
    z-index: 1;
    padding: 20px 0;

    ul {
        padding: 0px 20px;
        justify-content: space-between;
    }

    li {
        gap: 10px;
    }

    label {
        color: white;

        &:hover {
            cursor: pointer;
            filter: brightness(0);
        }
    }

    img {
        width: 35px;
        height: 40px;

        &:hover {
            cursor: pointer;
            filter: brightness(0);
        }
    }
}
</style>
