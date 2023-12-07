<script>
import BannerApp from './BannerApp.vue'
export default {
    data() {
        return {
            footerLinks: [
                {
                    title: "dc comics",
                    links: ["Character", "Comics", "Movies", "TV", "Games", "Videos", "News"]
                },
                {
                    title: "shops",
                    links: ["Shop DC", "Shop DC Collectibles"]
                },
                {
                    title: "dc",
                    links: ["Terms Of Use", "Privacy policy", "Ad Choices", "Advertising", "Jobs", "Subscriptions", "Talent Workshops", "CPSC Certificates", "Ratings", "Shop Help", "Contacts Us"]
                },
                {
                    title: "sites",
                    links: ["DC", "MAD Magazine", "DC Kids", "DC Universe", "DC Power Visa"]
                }
            ],
            logo: "public/img/dc-logo-bg.png",
            social: [
                "/img/footer-facebook.png", "/img/footer-twitter.png", "/img/footer-youtube.png", "/img/footer-pinterest.png", "/img/footer-periscope.png",
            ]
        }
    },
    components: {
        BannerApp,
    }
}
</script>

<template>
    <footer>
        <!-- footer top -->
        <BannerApp />
        <div class="cont-footer">
            <div class="cont-links">
                <div class="cont-bg">
                    <div class="footer-links">
                        <ul v-for="link in footerLinks">
                            <li class="title">{{ link.title }}</li>
                            <li v-for="prova in link.links">{{ prova }}</li>
                        </ul>
                    </div>
                    <div class="logo">
                        <img :src="logo" alt="">
                    </div>
                </div>
            </div>
        </div>
        <!-- /footer top -->

        <!-- footer bottom -->
        <div class="footer-bottom">
            <div class="cont">
                <button>sign-up now</button>
                <div class="icon">
                    <h3>follow us</h3>
                    <ul>
                        <li v-for="icon in social"><a href="#"><img :src="icon" alt="social"></a></li>
                    </ul>
                </div>
            </div>
        </div>
        <!-- footer bottom -->
    </footer>
</template>

<style scoped lang="scss">
@use '../style.scss' as *;

/* footer top */
.cont-links {
    background-image: url(/img/footer-bg.jpg);
    background-position: center;
    background-size: cover;
}

.cont-bg {
    display: flex;
    flex-direction: row;
    align-items: center;
    justify-content: space-between;
    max-width: $width-lg;
    max-height: 370px;
    overflow: hidden;
    margin: 0 auto;
}

.footer-links {
    color: #878869;
    display: flex;
    flex-direction: row;
    align-items: flex-start;
    flex-wrap: wrap;
    max-width: 500px;
    height: 100%;
    padding: 50px 0;
}

ul {
    margin-right: 10px;
}

ul li.title {
    color: white;
    font-weight: bold;
    font-size: 26px;
    text-transform: uppercase;
}

.logo {
    width: 50%;
}

/* footer bottom */
.footer-bottom {
    text-transform: uppercase;
    background-color: #303030;
}

.footer-bottom ul {
    display: flex;
    gap: 10px;
}

.footer-bottom .cont {
    display: flex;
    align-items: center;
    justify-content: space-between;
    padding: 20px;
    max-width: $width-lg;
    margin: 0 auto;
}

.icon {
    display: flex;
    align-items: center;
    gap: 10px;
}
</style>