<script>
export default {
    name: 'AppFooterTop',
    data: () => ({
        lists: {
            dcComicsItems: {
                title: 'Dc Comics',
                links: [
                    'Characters',
                    'Comics',
                    'Movies',
                    'TV',
                    'Games',
                    'Videos',
                    'News',
                ]
            },

            dcItems: {
                title: 'Dc',
                links: [
                    'Terms Of Use',
                    'Privacy policy (New)',
                    'Ad Choices',
                    'Advertising',
                    'Jobs',
                    'Talent Workshops',
                    'CPSC Certificates',
                    'Ratings',
                    'Shop Help',
                    'Contact Us',
                ]
            },

            sitesItems: {
                title: 'Sites',
                links: [
                    'DC',
                    'MAD Magazine',
                    'DC Kids',
                    'DC Universe',
                    'DC Power Visa',
                ]
            },

            shopItems: {
                title: 'Shop',
                links: [
                    'Shop DC',
                    'Shop DC Collectibles'
                ]
            },
        }
    }),


};
</script>
 
<template>
    <div class="footer-top">
        <div class="container flex">
            <div class="row">
                <div v-for="(list, i) in lists" :key="i" class="col">
                    <div class="list">
                        <h5>{{ list.title }}</h5>
                        <ul>
                            <li v-for="(link, i) in lists[i].links" :key="i"><a href="#">{{ list.links[i] }}</a></li>
                        </ul>
                    </div>
                </div>
            </div>
            <div class="right">
                <img src="../assets/img/dc-logo-bg.png" alt="">
            </div>
        </div>
    </div>
</template>
 
<style>
.footer-top {
    background-image: url(../assets/img/footer-bg.jpg);
    background-repeat: no-repeat;
    background-size: cover;
    height: calc(100vh - 280px);
    position: relative;
}

.footer-top>div {
    justify-content: space-between;
    align-items: normal;
}

.footer-top img {
    position: relative;
    bottom: 80px;
}

.footer-top .left {
    align-items: normal;
    padding: 20px 0;
    gap: 55px;
}

.list h5 {
    color: white;
    text-transform: uppercase;
}

.footer-top ul {
    text-transform: none;
    font-size: 0.6rem;
    margin-top: 10px;
}

.footer-top li {
    margin: 5px 0;
}

.footer-top a {
    color: grey;
}

.footer-top .row {
    display: flex;
    flex-wrap: wrap;
    column-gap: 25px;
    row-gap: 0px;
    margin-top: 20px;
    align-self: flex-start;
}

.footer-top .col {
    flex-basis: calc((100% / 3) - 50px / 3);
}

.footer-top li a:hover {
    filter: brightness(0);
}
</style>
