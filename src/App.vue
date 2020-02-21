<template>
  <div id="app">
    <div id="logo"><router-link to="/"><img src="./assets/main_logo.png"></router-link></div>
    <Menu></Menu>
    <MenuMobile></MenuMobile>
    <router-view></router-view>
    <Footer></Footer>
  </div>
</template>

<script>
import Menu from './components/Menu.vue';
import Footer from './components/Footer';
import MenuMobile from './components/MenuMobile.vue';
import "./style/default.css";

export default {
  name: 'app',
  components: {
    Menu,
    Footer,
    MenuMobile
  }
}
</script>

<style>
 
</style>
