<script>
export default {
    name: 'AppFooterTop',
    data: () => ({}),

    props: {
        footerTopList: Object
    }
};
</script>
 
<template>
    <div class="footer-top">
        <div class="container flex">
            <div class="row">
                <div v-for="(list, i) in footerTopList" :key="i" class="col">
                    <h5>{{ list.title }}</h5>
                    <ul>
                        <li v-for="(link, i) in footerTopList[i].links" :key="i"><a href="#">{{ list.links[i] }}</a></li>
                    </ul>
                </div>
            </div>
            <div class="right">
                <img src="../assets/img/dc-logo-bg.png" alt="">
            </div>
        </div>
    </div>
</template>
 
<style lang="scss" scoped>
.footer-top {
    background-image: url(../assets/img/footer-bg.jpg);
    background-repeat: no-repeat;
    background-size: cover;
    position: relative;
    padding: 10px 0px 20px 0px;

    .row {
        display: flex;
        flex-wrap: wrap;
        column-gap: 25px;
        row-gap: 0px;
        margin-top: 20px;
        align-self: flex-start;
    }

    .col {
        flex-basis: calc((100% / 3) - 50px / 3);

        h5 {
            color: white;
            text-transform: uppercase;
        }
    }

    ul {
        text-transform: none;
        font-size: 0.6rem;

        li {
            margin: 5px 0;
        }

    }

    img {
        position: absolute;
        width: 20%;
        right: 450px;
        bottom: 0px;
        top: -50px;
    }

    a {
        color: grey;
    }
}

.footer-top>div {
    justify-content: space-between;
    align-items: normal;
}

.footer-top li a:hover {
    filter: brightness(0);
}
</style>
