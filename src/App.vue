<template>
  <header-view></header-view>
  <router-view/>
</template>

<script>
import "./assets/style.css";
  import HeaderView from '@/components/HeaderView.vue';

export default {
  name: 'App',
  components: {
    HeaderView,
  }
}
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
</style>
