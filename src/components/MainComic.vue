<script>
export default {
    props: {
        img: String,
        title: String,
    }
}
</script>
<template>
    <div class="card">
        <div class="img-cont">
            <img :src="img" :alt="title">
        </div>
        <h3>{{ title }}</h3>
    </div>
</template>
<style lang="scss" scoped>
.img-cont {
    width: 180px;
    height: 180px;
}

img {
    width: 100%;
    height: 100%;
    display: block;
}
</style>