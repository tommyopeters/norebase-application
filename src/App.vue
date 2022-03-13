<template>
  <div id="app">
    <MobileMenu v-if="mobile" @mobile="mobile = false"></MobileMenu>
    <Header @mobile="mobile = true"></Header>
    <Main></Main>
    <Footer></Footer>
  </div>
</template>

<script>
import Header from "./components/layout/Header.vue";
import Footer from "./components/layout/Footer.vue";
import Main from "./components/layout/Main.vue";
import MobileMenu from "./components/layout/MobileMenu.vue";
// import LeftSideBar from "./components/layout/LeftSideBar.vue";
// import RightSideBar from "./components/layout/RightSideBar.vue";
import "./assets/sass/main.scss";

export default {
  name: "App",
  components: {
    Header,
    Footer,
    Main,
    MobileMenu,
    //  LeftSideBar,RightSideBar
  },
  data() {
    return {
      mobile: false,
    };
  },
};
</script>

//
<style lang="scss">
// #app {
//   font-family: Avenir, Helvetica, Arial, sans-serif;
//   -webkit-font-smoothing: antialiased;
//   -moz-osx-font-smoothing: grayscale;
//   text-align: center;
//   color: #2c3e50;
//   margin-top: 60px;
// }
//
</style>
