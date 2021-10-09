<template>
  <div class="container">
    <article>
      <h1 class="title">{{ album.title }} ({{ album.year }})</h1>
      <p>{{ album.content }}</p>
    </article>
    <aside>
      <h3>Other Albums</h3>
      <ul>
        <li v-for="related in relatedAlbums" :key="related.id">
          <nuxt-link :to="{ name: 'albums-id', params: { id: related.id } }">{{
            related.title
          }}</nuxt-link>
        </li>
      </ul>
    </aside>
  </div>
</template>

<script>
export default {
  data() {
    return {
      id: this.$route.params.id
    };
  },
  computed: {
    album() {
      return this.$store.state.albums.all.find(album => album.id === this.id);
    },
    relatedAlbums() {
      return this.$store.state.albums.all.filter(album => album.id !== this.id);
    }
  }
};
</script>

<style scoped>
.container {
  display: flex;
  justify-content: space-between;
  line-height: 1.5;
}
.article * {
  margin-bottom: 1rem;
}
.title {
  font-size: 2rem;
}
aside {
  min-width: 280px;
  max-width: 280px;
  padding-left: 2rem;
}
</style>
