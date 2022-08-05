<script setup lang="ts">

import { createApp } from 'vue'
import './style.css'

import { Quasar } from 'quasar'
import '@quasar/extras/material-icons-round/material-icons-round.css'

import { Nuxt } from 'nuxt'

import HelloWorld from './components/HelloWorld.vue'
import { ref } from 'vue'

const App = Vue.create()

createApp(App)
.use(Quasar)
.mount('#app')

const tab = ref('mail')

</script>
<!-- <script>
export default {
  name: 'App'
}
</script> -->

<template>
  <NuxtPage />

  <q-tabs
    v-model="tab"
    class="text-teal"
  >
    <q-tab name="mails" icon="mail" label="Mails" />
    <q-tab name="alarms" icon="alarm" label="Alarms" />
    <q-tab name="movies" icon="movie" label="Movies" />
  </q-tabs>

  <div>
    <a href="https://vitejs.dev" target="_blank">
      <img src="/vite.svg" class="logo" alt="Vite logo" />
    </a>
    <a href="https://vuejs.org/" target="_blank">
      <img src="./assets/vue.svg" class="logo vue" alt="Vue logo" />
    </a>
  </div>
  <HelloWorld msg="Vite + Vue" />

</template>

<style scoped>
.logo {
  height: 6em;
  padding: 1.5em;
  will-change: filter;
}
.logo:hover {
  filter: drop-shadow(0 0 2em #646cffaa);
}
.logo.vue:hover {
  filter: drop-shadow(0 0 2em #42b883aa);
}
</style>
