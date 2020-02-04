<template>
  <div id="app" class="bg-dark h-screen">
    <app-header />
    <div class="container">
      <app-sounds />
    </div>
  </div>
</template>

<script>
import AppHeader from '@/components/Header.vue'
import AppSounds from '@/components/Sounds.vue'

export default {
  name: 'app',
  components: {
    AppSounds,
    AppHeader
  }
}
</script>

<style>
@import 'assets/css/tailwind.css';
</style>
