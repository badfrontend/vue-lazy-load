<template>
  <div id="app">
    <div class="container">
      <Navigation />
      <router-view/>
    </div>
  </div>
</template>


<script>
import Navigation from '@/components/Navigation/index.vue';

export default {
  components: {
    Navigation,
  },
};
</script>


<style lang="scss">
.container {
  grid-column: span 1;
  display: grid;
  grid-template-columns: 1fr;
  padding: 0 20px;
  @media (min-width: 740px) {
    grid-template-columns: 1fr repeat(10, 80px) 1fr;
  }
}
</style>
