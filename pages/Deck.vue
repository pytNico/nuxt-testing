<template>
  <div>
    <h1>Nuxt-Testing Deck</h1>
    <hr />

    <vue-masonry-wall
      :items="items"
      :options="{ width: 300, padding: 12 }"
      @append="append"
    >
      <template v-slot:default="{ item }">
        <div class="item">
          <h5>{{ item.title }}</h5>
          <p>{{ item.content }}</p>
        </div>
      </template>
    </vue-masonry-wall>
  </div>
</template>

<script>
import VueMasonryWall from 'vue-masonry-wall'

export default {
  name: 'app',
  components: { VueMasonryWall },
  data() {
    return {
      items: [
        { title: 'Item 0', content: 'Content' },
        { title: 'Item 1', content: 'Content' },
      ],
    }
  },
  methods: {
    append() {
      for (let i = 0; i < 20; i++) {
        this.items.push({
          title: `Item ${this.items.length}`,
          content: 'Content',
        })
      }
    },
  },
}
</script>

<style scoped></style>
