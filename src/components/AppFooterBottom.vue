<script>
export default {
    name: 'AppFooterBottom',
    data: () => ({}),

    props: {
        footerBottomIcons: Object
    },

    methods: {
        createPath() {
            const url = new URL(`../assets/img/`, import.meta.url)
            return url.href
        }
    }
};
</script>
 
<template>
    <div class="footer-bottom">
        <div class="container flex">
            <div class="left">
                <button>
                    <h5>SIGN-UP NOW!</h5>
                </button>
            </div>
            <div class="right">
                <a href="#">
                    <h5>FOLLOW US</h5>
                </a>
                <ul class="flex">
                    <li v-for="(link, i) in footerBottomIcons.links" :key="i"><a href="#"><img
                                :src="`${createPath()}/${link}`" alt=""></a>
                    </li>
                </ul>
            </div>
        </div>
    </div>
</template>
 
<style lang="scss" scoped>
.footer-bottom {
    // height: 70px;
    background-color: rgb(48, 48, 48);
    position: sticky;
    filter: drop-shadow(2px 4px 6px black);

    button {
        color: white;
        border: 1px solid rgb(12, 105, 247);
        background-color: rgb(48, 48, 48);
        padding: 10px;

        &:hover {
            cursor: pointer;
        }
    }

    .right {
        display: flex;
        align-items: center;

        h5 {
            color: rgb(12, 105, 247);
            margin: 0 20px
        }

        li:hover {
            filter: brightness(0);
        }

    }
}

.footer-bottom>div {
    justify-content: space-between;
    align-items: center;
    height: 90px;
}
</style>
