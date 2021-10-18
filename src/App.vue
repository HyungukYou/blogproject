<template>
  <div id="app">
    <nav class="navbar navbar-light bg-light">
      <a class="navbar-brand">Navbar</a>
      <form class="form-inline">
        <input class="form-control mr-sm-2" type="search" placeholder="Search" aria-label="Search">
        <button class="btn btn-outline-success my-2 my-sm-0" type="submit">Search</button>
      </form>
    </nav>

    <div class="container">
      <h5>개발자의 블로그입니다</h5>
      <P> Vue로 만들었음 </P>
    </div>

    <router-view :blog="블로그글"></router-view>
<!--    <List :blog="블로그글"/>-->

  </div>
</template>

<script>
// import List from './components/List.vue';
import blog from './assets/blog.js';
export default {
  name: 'App',
  data(){
    return {
      블로그글 : blog,
    }
  },
  components: {
    // List

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
