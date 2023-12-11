<script>
export default {}
</script>

<template>
    <div class="jumbo">
        <h2>Current Series</h2>
    </div>
</template>

<style lang="scss" scoped>
@use '../assets/scss/partials/variables.scss' as *;

.jumbo {
    position: relative;
    height: 400px;
    background-image: url(../assets/img/jumbotron.jpg);
    background-position: top;
    background-size: cover;

    h2 {
        padding: 15px 30px;
        background-color: $color-banner;
        position: absolute;
        bottom: -30px;
        left: 200px;
        color: white;
        text-transform: uppercase;
    }
}
</style>