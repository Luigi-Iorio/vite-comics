<script>
import FooterBanner from './FooterBanner.vue'
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
                "src/assets/img/footer-facebook.png", "src/assets/img/footer-twitter.png", "src/assets/img/footer-youtube.png", "src/assets/img/footer-pinterest.png", "src/assets/img/footer-periscope.png",
            ]
        }
    },
    components: {
        FooterBanner,
    }
}
</script>

<template>
    <footer>
        <!-- footer top -->
        <FooterBanner />
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
@use '../assets/scss/partials/variables.scss' as *;

/* footer top */
.cont-links {
    background-image: url(../assets/img/footer-bg.jpg);
    background-position: center;
    background-size: cover;
}

.cont-bg {
    display: flex;
    flex-direction: row;
    align-items: flex-start;
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
    flex-wrap: wrap;
    margin-top: 35px;
    max-width: 400px;
    height: 100%;
    gap: 30px;

    ul {
        height: 200px;
        margin-right: 5px;
        display: flex;
        flex-direction: column;
        gap: 5px;

        li.title {
            color: white;
            font-weight: bold;
            font-size: 26px;
            text-transform: uppercase;
        }
    }

}

ul:nth-last-of-type(3) {
    order: 1;
}

.logo {
    width: 50%;
    align-self: center;
}

/* footer bottom */
.footer-bottom {
    text-transform: uppercase;
    background-color: $color-footer-bottom;

    ul {
        display: flex;
        gap: 10px;
    }

    .cont {
        display: flex;
        align-items: center;
        justify-content: space-between;
        padding: 30px 0;
        max-width: $width-lg;
        margin: 0 auto;
    }

    button {
        padding: 10px 15px;
        border: 2px solid $color-banner;
        background-color: $color-footer-bottom;
        color: white;
        text-transform: uppercase;
        font-weight: bold;
    }

    .icon {
        display: flex;
        align-items: center;
        gap: 10px;

        h3 {
            color: $color-banner;
        }
    }
}
</style>