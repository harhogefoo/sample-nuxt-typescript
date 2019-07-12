<template>
  <div class="container">
    <div>
      <logo />
      <h1 class="title">
        sample-nuxt-typescript
      </h1>
      <h2 class="subtitle">
        My magnificent Nuxt.js project
      </h2>
      <div class="links">
        <a href="https://nuxtjs.org/" target="_blank" class="button--green">
          Documentation
        </a>
        <a
          href="https://github.com/nuxt/nuxt.js"
          target="_blank"
          class="button--grey"
        >
          GitHub
        </a>
      </div>
      <div class="actions">
        <a class="button--action" @click="addTada">🎉 {{ tada }}</a>
        <a class="button--action" @click="addSparkles">✨ {{ sparkles }}</a>
        <a class="button--action" @click="addThumbsup">👍 {{ thumbsup }}</a>
        <a class="button--action" @click="addHeart">🧡 {{ heart }}</a>
        <a class="button--clear" @click="clear">Clear</a>
      </div>
    </div>
  </div>
</template>

<script lang="ts">
import { Component, Vue } from 'vue-property-decorator'

@Component({
  components: {
    Logo: () => import('~/components/Logo.vue'),
  },
})
export default class Index extends Vue {
  tada: number = 0

  sparkles: number = 0

  thumbsup: number = 0

  heart: number = 0

  addTada() {
    this.tada++
  }

  addSparkles() {
    this.sparkles++
  }

  addThumbsup() {
    this.thumbsup++
  }

  addHeart() {
    this.heart++
  }

  clear() {
    this.tada = 0
    this.sparkles = 0
    this.thumbsup = 0
    this.heart = 0
  }
}
</script>

<style>
.container {
  margin: 0 auto;
  min-height: 100vh;
  display: flex;
  justify-content: center;
  align-items: center;
  text-align: center;
}

.title {
  font-family: 'Quicksand', 'Source Sans Pro', -apple-system, BlinkMacSystemFont,
    'Segoe UI', Roboto, 'Helvetica Neue', Arial, sans-serif;
  display: block;
  font-weight: 300;
  font-size: 100px;
  color: #35495e;
  letter-spacing: 1px;
}

.subtitle {
  font-weight: 300;
  font-size: 42px;
  color: #526488;
  word-spacing: 5px;
  padding-bottom: 15px;
}

.links {
  padding-top: 15px;
}
</style>
