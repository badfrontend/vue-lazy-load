<template>
  <div class="home">
    <img alt="Vue logo" src="../assets/logo.png">
    <HelloWorld msg="Welcome to Your Vue.js App"/>
  </div>
</template>

<script>
// @ is an alias to /src
import HelloWorld from '@/components/HelloWorld.vue';

export default {
  name: 'home',
  data() {
    return {
      films: null,
    };
  },
  components: {
    HelloWorld,
  },
  async mounted() {
    const films = await this.$axios.get('/people/');
    this.films = films.data;
  },
};
</script>

<style lang="scss" scoped>
.home {
  grid-column: 2/3;
}
</style>
