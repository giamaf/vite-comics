<script>
export default {
    name: 'AppHeader',
    data: () => ({}),
    props: {
        links: Array
    }
};
</script>
 
<template>
    <header class="flex container">
        <a href="#"><img src="../assets/img/dc-logo.png" alt=""></a>
        <ul class="flex">
            <li v-for="(link, i) in   links  " :key="i">
                <a :href="link.url">{{ link.text }}</a>
            </li>
        </ul>
    </header>
</template>
 
<style lang="scss" scoped>
header {
    justify-content: space-between;
    height: 80px;
    font-size: 0.7rem;
    font-weight: bold;

    img {
        width: 50px;
        height: 50px;
    }

    a {
        color: black;

        &:hover {
            color: blue;
        }
    }
}
</style>
