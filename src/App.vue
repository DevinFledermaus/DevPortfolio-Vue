<template>
  <Header />
  <router-view/>
</template>

<script>
import Header from './components/Header.vue'

export default {
  components: { Header },
  setup() {
    window.addEventListener("scroll",function() {
      const header = document.querySelector('header');
      header.classList.toggle('sticky', window.scrollY > 0)
    });

    // const navigation = document.querySelector('nav');
    // document.querySelector('.toggle').onclick = function() {
    //   this.classList.toggle('active');
    //   navigation.classList.toggle('active');
    // }
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
  background: url(./assets/sugar-skull.jpg);
  background-position: center;
  background-repeat: no-repeat;
  background-size: cover;
  background-attachment: fixed;
}
</style>
