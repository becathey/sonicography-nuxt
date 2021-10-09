<template>
  <section class="container">
    <div>
      <h1 class="title"><span class="sonic">sonic</span>ography</h1>
      <h2 class="subtitle">Studio Albums of Sonic Youth</h2>
      <div class="links">
        <nuxt-link
          v-for="album in albums"
          :to="{ name: 'albums-id', params: { id: album.id } }"
          :key="album.id"
          class="button-green"
          >{{ album.title }}</nuxt-link
        >
      </div>
    </div>
  </section>
</template>

<script>
export default {
  computed: {
    albums() {
      return this.$store.state.albums.all;
    }
  }
};
</script>

<style scoped>
.container {
  display: flex;
  align-items: center;
  justify-content: center;
  text-align: center;
}
.title {
  display: block;
  font-family: "Segoe UI", Tahoma, Geneva, Verdana, sans-serif;
  font-size: 60px;
  font-weight: bold;
  letter-spacing: 1px;
}
.subtitle {
  color: hsl(220, 20%, 50%);
  font-size: 32px;
  font-weight: 300;
  word-spacing: 5px;
}
.links {
  margin-top: 30px;
  /* padding-top: 15px; */
}
</style>
