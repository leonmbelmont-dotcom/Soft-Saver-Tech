<script setup>
import { RouterView } from 'vue-router'
import SiteHeader from './components/SiteHeader.vue'
import SiteNav from './components/SiteNav.vue'
import SiteFooter from './components/SiteFooter.vue'
</script>

<template>
  <div id="app">
    <SiteNav />
    <SiteHeader />
    <main class="app-main">
      <RouterView />
    </main>
    <SiteFooter />
  </div>
</template>

<style scoped>
#app {
  min-height: 100vh;
  display: flex;
  flex-direction: column;
}

.app-main {
  width: 100%;
  max-width: 1100px;
  margin: 0 auto;
  padding: 3rem 1.5rem 2rem;
}

@media (min-width: 900px) {
  .app-main {
    padding: 3rem 2rem 2rem;
  }
}
</style>
