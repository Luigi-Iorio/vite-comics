<script>
export default {};
</script>

<template>
    <main>
        <div class="cont">
            <h2>Content goes here</h2>
        </div>
    </main>
</template>

<style lang="scss" scoped>
@use '../style.scss' as *;

main {
    background-color: #1c1c1c;
    padding: 20px;
}

.cont {
    max-width: $width-lg;
    margin: 0 auto;
}

h2 {
    color: white;
}
</style>
