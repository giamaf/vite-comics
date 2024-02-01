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
    <header class="flex container">
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
    min-height: 80px;
    font-size: 0.7rem;
    font-weight: bold;
}

header img {
    width: 50px;
    height: 50px;
}

header a {
    color: black;
}
</style>
