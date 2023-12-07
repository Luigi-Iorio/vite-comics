<script>
export default {
  data() {
    return {
      logo: "/img/dc-logo.png",
      headerLinks: ["characters", "comics", "movies", "tv", "games", "collectibles", "videos", "fans", "news", "shop"]
    }
  }
}
</script>

<template>
  <header>
    <nav>
      <!-- logo -->
      <div class="logo">
        <img :src="logo" alt="logo dc">
      </div>
      <!-- /logo -->

      <!-- header links -->
      <ul>
        <li v-for="link in headerLinks"><a href="#">{{ link }}</a></li>
      </ul>
      <!-- /header links -->
    </nav>
  </header>
</template>

<style scoped>
header {
  padding: 20px;
  text-transform: uppercase;
}

nav {
  display: flex;
  flex-direction: row;
  align-items: center;
  justify-content: space-between;
  max-width: 1200px;
  margin: 0 auto;

}

ul {
  display: flex;
  flex-direction: row;
  gap: 20px
}
</style>
