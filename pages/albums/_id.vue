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
      id: this.$route.params.id,
      albums: [
        {
          id: "confusion",
          title: "Confusion Is Sex",
          year: 1983,
          content:
            "Lorem ipsum dolor sit amet, consectetur adipisicing elit. Dolorem qui, asperiores architecto, pariatur consequuntur dicta hic dolorum consectetur laudantium iusto placeat eaque cumque, odit saepe! Voluptates perspiciatis ullam consequatur architecto esse, eligendi voluptatum obcaecati eius temporibus velit vero earum ea. Esse expedita illum dolor magni, accusantium ipsam. Velit, esse ex!"
        },
        {
          id: "badMoon",
          title: "Bad Moon Rising",
          year: 1985,
          content:
            "Lorem ipsum dolor sit amet, consectetur adipisicing elit. Dolorem qui, asperiores architecto, pariatur consequuntur dicta hic dolorum consectetur laudantium iusto placeat eaque cumque, odit saepe! Voluptates perspiciatis ullam consequatur architecto esse, eligendi voluptatum obcaecati eius temporibus velit vero earum ea. Esse expedita illum dolor magni, accusantium ipsam. Velit, esse ex!"
        },
        {
          id: "evol",
          title: "Evol",
          year: 1986,
          content:
            "Lorem ipsum dolor sit amet, consectetur adipisicing elit. Dolorem qui, asperiores architecto, pariatur consequuntur dicta hic dolorum consectetur laudantium iusto placeat eaque cumque, odit saepe! Voluptates perspiciatis ullam consequatur architecto esse, eligendi voluptatum obcaecati eius temporibus velit vero earum ea. Esse expedita illum dolor magni, accusantium ipsam. Velit, esse ex!"
        },
        {
          id: "sister",
          title: "Sister",
          year: 1987,
          content:
            "Lorem ipsum dolor sit amet, consectetur adipisicing elit. Dolorem qui, asperiores architecto, pariatur consequuntur dicta hic dolorum consectetur laudantium iusto placeat eaque cumque, odit saepe! Voluptates perspiciatis ullam consequatur architecto esse, eligendi voluptatum obcaecati eius temporibus velit vero earum ea. Esse expedita illum dolor magni, accusantium ipsam. Velit, esse ex!"
        },
        {
          id: "daydream",
          title: "Daydream Nation",
          year: 1988,
          content:
            "Lorem ipsum dolor sit amet, consectetur adipisicing elit. Dolorem qui, asperiores architecto, pariatur consequuntur dicta hic dolorum consectetur laudantium iusto placeat eaque cumque, odit saepe! Voluptates perspiciatis ullam consequatur architecto esse, eligendi voluptatum obcaecati eius temporibus velit vero earum ea. Esse expedita illum dolor magni, accusantium ipsam. Velit, esse ex!"
        },
        {
          id: "goo",
          title: "Goo",
          year: 1990,
          content:
            "Lorem ipsum dolor sit amet, consectetur adipisicing elit. Dolorem qui, asperiores architecto, pariatur consequuntur dicta hic dolorum consectetur laudantium iusto placeat eaque cumque, odit saepe! Voluptates perspiciatis ullam consequatur architecto esse, eligendi voluptatum obcaecati eius temporibus velit vero earum ea. Esse expedita illum dolor magni, accusantium ipsam. Velit, esse ex!"
        },
        {
          id: "dirty",
          title: "Dirty",
          year: 1992,
          content:
            "Lorem ipsum dolor sit amet, consectetur adipisicing elit. Dolorem qui, asperiores architecto, pariatur consequuntur dicta hic dolorum consectetur laudantium iusto placeat eaque cumque, odit saepe! Voluptates perspiciatis ullam consequatur architecto esse, eligendi voluptatum obcaecati eius temporibus velit vero earum ea. Esse expedita illum dolor magni, accusantium ipsam. Velit, esse ex!"
        },
        {
          id: "jetSet",
          title: "Experimental Jet Set, Trash and No Star",
          year: 1994,
          content:
            "Lorem ipsum dolor sit amet, consectetur adipisicing elit. Dolorem qui, asperiores architecto, pariatur consequuntur dicta hic dolorum consectetur laudantium iusto placeat eaque cumque, odit saepe! Voluptates perspiciatis ullam consequatur architecto esse, eligendi voluptatum obcaecati eius temporibus velit vero earum ea. Esse expedita illum dolor magni, accusantium ipsam. Velit, esse ex!"
        },
        {
          id: "washingMachine",
          title: "Washing Machine",
          year: 1995,
          content:
            "Lorem ipsum dolor sit amet, consectetur adipisicing elit. Dolorem qui, asperiores architecto, pariatur consequuntur dicta hic dolorum consectetur laudantium iusto placeat eaque cumque, odit saepe! Voluptates perspiciatis ullam consequatur architecto esse, eligendi voluptatum obcaecati eius temporibus velit vero earum ea. Esse expedita illum dolor magni, accusantium ipsam. Velit, esse ex!"
        },
        {
          id: "leaves",
          title: "A Thousand Leaves",
          year: 1998,
          content:
            "Lorem ipsum dolor sit amet, consectetur adipisicing elit. Dolorem qui, asperiores architecto, pariatur consequuntur dicta hic dolorum consectetur laudantium iusto placeat eaque cumque, odit saepe! Voluptates perspiciatis ullam consequatur architecto esse, eligendi voluptatum obcaecati eius temporibus velit vero earum ea. Esse expedita illum dolor magni, accusantium ipsam. Velit, esse ex!"
        },
        {
          id: "ghosts",
          title: "NYC Ghosts & Flowers",
          year: 2000,
          content:
            "Lorem ipsum dolor sit amet, consectetur adipisicing elit. Dolorem qui, asperiores architecto, pariatur consequuntur dicta hic dolorum consectetur laudantium iusto placeat eaque cumque, odit saepe! Voluptates perspiciatis ullam consequatur architecto esse, eligendi voluptatum obcaecati eius temporibus velit vero earum ea. Esse expedita illum dolor magni, accusantium ipsam. Velit, esse ex!"
        },
        {
          id: "murray",
          title: "Murray Street",
          year: 2002,
          content:
            "Lorem ipsum dolor sit amet, consectetur adipisicing elit. Dolorem qui, asperiores architecto, pariatur consequuntur dicta hic dolorum consectetur laudantium iusto placeat eaque cumque, odit saepe! Voluptates perspiciatis ullam consequatur architecto esse, eligendi voluptatum obcaecati eius temporibus velit vero earum ea. Esse expedita illum dolor magni, accusantium ipsam. Velit, esse ex!"
        },
        {
          id: "nurse",
          title: "Sonic Nurse",
          year: 2004,
          content:
            "Lorem ipsum dolor sit amet, consectetur adipisicing elit. Dolorem qui, asperiores architecto, pariatur consequuntur dicta hic dolorum consectetur laudantium iusto placeat eaque cumque, odit saepe! Voluptates perspiciatis ullam consequatur architecto esse, eligendi voluptatum obcaecati eius temporibus velit vero earum ea. Esse expedita illum dolor magni, accusantium ipsam. Velit, esse ex!"
        },
        {
          id: "ripped",
          title: "Rather Ripped",
          year: 2006,
          content:
            "Lorem ipsum dolor sit amet, consectetur adipisicing elit. Dolorem qui, asperiores architecto, pariatur consequuntur dicta hic dolorum consectetur laudantium iusto placeat eaque cumque, odit saepe! Voluptates perspiciatis ullam consequatur architecto esse, eligendi voluptatum obcaecati eius temporibus velit vero earum ea. Esse expedita illum dolor magni, accusantium ipsam. Velit, esse ex!"
        },
        {
          id: "eternal",
          title: "The Eternal",
          year: 2009,
          content:
            "Lorem ipsum dolor sit amet, consectetur adipisicing elit. Dolorem qui, asperiores architecto, pariatur consequuntur dicta hic dolorum consectetur laudantium iusto placeat eaque cumque, odit saepe! Voluptates perspiciatis ullam consequatur architecto esse, eligendi voluptatum obcaecati eius temporibus velit vero earum ea. Esse expedita illum dolor magni, accusantium ipsam. Velit, esse ex!"
        }
      ]
    };
  },
  computed: {
    album() {
      return this.albums.find(album => album.id === this.id);
    },
    relatedAlbums() {
      return this.albums.filter(album => album.id !== this.id);
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
