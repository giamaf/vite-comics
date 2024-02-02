<script>
export default {
    name: 'AppFooterTop',
    data: () => ({
        footerIcons: {
            links: [
                'footer-facebook.png',
                'footer-twitter.png',
                'footer-youtube.png',
                'footer-pinterest.png',
                'footer-periscope.png'
            ]
        },
    }),

    methods: {
        createPath(path) {
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
                <button role="button">
                    <h5>SIGN-UP NOW!</h5>
                </button>
            </div>
            <div class="right">
                <a href="#">
                    <h5>FOLLOW US</h5>
                </a>
                <ul class="flex">
                    <li class="social-link" v-for="(link, i) in footerIcons.links" :key="i"><a href="#"><img
                                :src="`${createPath()}/${link}`" alt=""></a>
                    </li>
                </ul>
            </div>
        </div>
    </div>
</template>
 
<style>
.footer-bottom {
    height: 90px;
    background-color: rgb(48, 48, 48);
    filter: drop-shadow(2px 4px 6px black);
}

.footer-bottom>div {
    justify-content: space-between;
    align-items: center;
    height: 90px;
}

.footer-bottom button {
    color: white;
    border: 1px solid rgb(12, 105, 247);
    background-color: rgb(48, 48, 48);
    padding: 10px;
}

.footer-bottom .right {
    display: flex;
    align-items: center;
}

.footer-bottom .right h5 {
    color: rgb(12, 105, 247);
    margin: 0 20px
}

.social-link img {
    width: 25px;
    height: 25px;

}

.footer-bottom button:hover {
    cursor: pointer;
}

.footer-bottom .social-link:hover {
    filter: brightness(0);
}
</style>
