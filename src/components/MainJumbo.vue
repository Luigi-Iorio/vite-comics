<script>
export default {}
</script>

<template>
    <div class="jumbo">
        <div class="cont">
            <h2>Current Series</h2>
        </div>
    </div>
</template>

<style lang="scss" scoped>
@use '../assets/scss/partials/variables.scss' as *;

.jumbo {
    height: 400px;
    background-image: url(../assets/img/jumbotron.jpg);
    background-position: top;
    background-size: cover;

    .cont {
        position: relative;
        width: $width-lg;
        height: 100%;
        margin: 0 auto;

        h2 {
            padding: 15px 30px;
            background-color: $color-banner;
            position: absolute;
            bottom: -30px;
            left: 0;
            color: white;
            text-transform: uppercase;
        }
    }
}
</style>