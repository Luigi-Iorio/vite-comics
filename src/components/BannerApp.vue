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
            ]
        }
    }
}
</script>

<template>
    <div class="cont">
        <ul>
            <li v-for="buy in listBuy">
                <div class="image">
                    <img :src="buy.img" :alt="text">
                </div>
                <h6>{{ buy.text }}</h6>
            </li>
        </ul>
    </div>
</template>

<style scoped>
.cont {
    background-color: #0282f9;
    padding: 20px;
    text-transform: uppercase;
}

ul {
    display: flex;
    flex-direction: row;
    justify-content: center;
    max-width: 1200px;
    margin: 0 auto;
    gap: 50px;
}

li {
    display: flex;
    flex-direction: row;
    align-items: center;
    gap: 10px;
}

.image {
    width: 60px;
}

.image img {
    width: 100%;
    display: block;
}
</style>