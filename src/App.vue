<script setup>
import PostList from './components/PostList.vue'
import NavBart from './components/NavBart.vue';
import NavFooter from './components/NavFooter.vue';
</script>

<template>
  <header>
    <NavBart/>
  </header>

  <main>
      <PostList />
  </main>

  <footer>
    <NavFooter/>
  </footer>

</template>

<style scoped>

</style>
