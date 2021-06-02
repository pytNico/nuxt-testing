<template>
  <div>
    <h1>Nuxt-Testing Deck</h1>
    <hr />

    <vue-masonry-wall
      :items="items"
      :options="{ width: 300, padding: 12 }"
      @append="append"
      :ssr="{ columns: 2 }"
    >
      <template v-slot:default="{ item }">
        <b-card
          :title="item.title"
          :img-src="item.imgSrc"
          img-alt="Image"
          img-top
          tag="article"
          style="max-width: 20rem"
          class="mb-2"
        >
          <b-card-text>
            {{ item.content }}
          </b-card-text>

          <b-button href="#" variant="primary">Test</b-button>
        </b-card>
      </template>
    </vue-masonry-wall>
  </div>
</template>

<script>
import VueMasonryWall from 'vue-masonry-wall'

export default {
  name: 'Deck',
  components: { VueMasonryWall },
  data() {
    return {
      items: [
        {
          title: 'Item 0',
          imgSrc: 'https://via.placeholder.com/350x600',
          content: 'Content',
        },
        {
          title: 'Item 1',
          imgSrc: 'https://via.placeholder.com/1000x1000',
          content: 'Content',
        },
        {
          title: 'Item 2',
          imgSrc: 'https://via.placeholder.com/600x350',
          content: 'Content',
        },
      ],
    }
  },
  methods: {
    append() {
      for (let i = 0; i < 20; i++) {
        var rndInt1 = Math.floor(Math.random() * (1000 - 150 + 1) + 150)
        var rndInt2 = Math.floor(Math.random() * (500 - 500 + 1) + 500)
        this.items.push({
          title: `Item ${this.items.length}`,
          //imgSrc: `https://via.placeholder.com/${rndInt1}x${rndInt2}`,
          imgSrc: `https://picsum.photos/${rndInt1}/${rndInt2}?random`,
          content:
            'Lorem ipsum dolor sit amet, consectetur adipiscing elit. Nullam leo neque, scelerisque ut tellus non, posuere pretium leo. Donec laoreet.',
        })
      }
    },
  },
}
</script>

<style>
.masonry-item {
  align-self: center;
}
</style>
