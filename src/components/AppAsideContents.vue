<script>
export default {
    name: 'AppAsideContents',


    data: () => ({
        asideItems: [
            {
                image: 'buy-comics-digital-comics.png',
                label: 'Digital Comics'
            },
            {
                image: 'buy-comics-merchandise.png',
                label: 'Dc Merchandise'
            },
            {
                image: 'buy-comics-subscriptions.png',
                label: 'Subscription'
            },
            {
                image: 'buy-comics-shop-locator.png',
                label: 'Comic Shop Locator'
            },
            {
                image: 'buy-dc-power-visa.svg',
                label: 'Dc Power Visa'
            }
        ]
    }),
    methods: {
        createPath(path) {
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
                <li v-for="(item, i) in asideItems" :key="i" class="flex">
                    <a href="#"><img :src="`${createPath()}/${item.image}`" :alt="item.label"></a>
                    <label for="">{{ item.label }}</label>
                </li>
            </ul>
        </div>
    </aside>
</template>
 
<style>
aside {
    background-color: rgb(12, 105, 247);
    min-height: 100px;
    font-size: 0.7rem;
}

aside ul {
    padding: 0 20px;
    justify-content: space-between;
}

aside li {
    gap: 10px;
    height: 100px;
}

aside label {
    color: white;
    line-height: 100px;
}

aside img {
    width: 35px;
    height: 40px;
    margin-left: 10px;
}
</style>
