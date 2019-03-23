<template>
  <div class="navigation">
    <router-link to="/">Фильмы</router-link>
    <router-link to="/about">Персонажи</router-link>
    <router-link to="/about">Планеты</router-link>
    <router-link to="/about">Виды</router-link>
  </div>
</template>

<style lang="scss" scoped>
.navigation {
  padding: 30px;
  grid-column: 2/12;
  a {
    font-weight: bold;
    color: #2c3e50;
    &.router-link-exact-active {
      color: #42b983;
    }
  }
}
</style>
