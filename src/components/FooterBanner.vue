<script>
export default {
    data() {
        return {
            listBuy: [
                {
                    img: "/img/buy-comics-digital-comics.png",
                    text: "digital comics",
                },
                {
                    img: "/img/buy-comics-merchandise.png",
                    text: "dc merchandise",
                },
                {
                    img: "/img/buy-comics-shop-locator.png",
                    text: "subscription",
                },
                {
                    img: "/img/buy-comics-subscriptions.png",
                    text: "comic shop locator",
                },
                {
                    img: "/img/buy-dc-power-visa.svg",
                    text: "dc power visa",
                },
            ],
        };
    },
};
</script>

<template>
    <div class="cont">
        <ul>
            <li v-for="buy in listBuy">
                <div class="image">
                    <img :src="buy.img" :alt="text" />
                </div>
                <p>{{ buy.text }}</p>
            </li>
        </ul>
    </div>
</template>

<style scoped lang="scss">
@use "../assets/scss/partials/variables.scss" as *;

.cont {
    background-color: $color-banner;
    padding: 50px 20px;
    text-transform: uppercase;
    color: white;

    ul {
        display: flex;
        flex-direction: row;
        justify-content: center;
        max-width: $width-lg;
        margin: 0 auto;
        gap: 50px;

        li {
            display: flex;
            flex-direction: row;
            align-items: center;
            gap: 10px;

            .image {
                width: 60px;
                height: 60px;

                & img {
                    width: 100%;
                    height: 100%;
                    object-fit: contain;
                }
            }
        }
    }
}

p {
    font-size: 15px;
}
</style>
