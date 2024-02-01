<script>
export default {
    name: 'AppHeader',
    data: () => ({
        navItems: [
            {
                text: 'Characters',
                url: '#',
                current: false,
            },
            {
                text: 'Comics',
                url: '#',
                current: true,
            },
            {
                text: 'Movies',
                url: '#',
                current: false,
            },
            {
                text: 'TV',
                url: '#',
                current: false,
            },
            {
                text: 'Games',
                url: '#',
                current: false,
            },
            {
                text: 'Collectibles',
                url: '#',
                current: false,
            },
            {
                text: 'Videos',
                url: '#',
                current: false,
            },
            {
                text: 'Fans',
                url: '#',
                current: false,
            },
            {
                text: 'News',
                url: '#',
                current: false,
            },
            {
                text: 'Shop',
                url: '#',
                current: false,
            },
        ]
    }),


};
</script>
 
<template>
    <header class="flex">
        <a href="#"><img src="../assets/img/dc-logo.png" alt=""></a>
        <ul class="flex">
            <li v-for="(item, i) in   navItems  " :key="i">
                <a :href="item.url">{{ item.text }}</a>
            </li>
        </ul>
    </header>
</template>
 
<style>
header {
    justify-content: space-between;
    min-height: 70px;
    font-size: 0.7rem;
    font-family: 'Open Sans Condensed';
    font-weight: bold;
}

img {
    width: 50px;
    height: 50px;
}

ul {
    text-transform: uppercase;
    gap: 20px;
}
</style>
