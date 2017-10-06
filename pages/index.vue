<template>
  <section class="container">
    <div>
      <logo/>
      <h1 class="title">
        vue-swal-app
      </h1>
      <h2 class="subtitle">
        Nuxt project with VueSwal
      </h2>
      <div class="links">
        <a href="" @click.prevent="go" class="button--green">Get Started!</a>
        <a href="https://github.com/anteriovieria/vue-swal" target="_blank" class="button--grey">GitHub</a>
      </div>
    </div>
  </section>
</template>

<script>
import Logo from '~/components/Logo.vue'

export default {
  methods: {
    go () {
      this.$swal('Good job!', 'You are ready to start!', 'success').then(() => {
        window.location = 'https://github.com/anteriovieira/vue-swal#vueswal'
      })
    }
  },
  components: {
    Logo
  }
}
</script>

<style>
.container {
  min-height: 100vh;
  display: flex;
  justify-content: center;
  align-items: center;
  text-align: center;
}

.title {
  font-family: "Quicksand", "Source Sans Pro", -apple-system, BlinkMacSystemFont, "Segoe UI", Roboto, "Helvetica Neue", Arial, sans-serif; /* 1 */
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
