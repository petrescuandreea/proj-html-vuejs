<template>
  <div id="app">
    <header>
      <AppHeader :links="headerNavLinks"/>
    </header>


    <main>
      <AppMain/>
    </main>

    <footer>
      <AppFooter/>
    </footer>
    
  </div>
</template>

<script>
import AppHeader from './components/AppHeader.vue';
import AppMain from './components/AppMain.vue';
import AppFooter from './components/AppFooter.vue';

export default {
  name: 'App',
  components: {
    AppHeader,
    AppMain,
    AppFooter
  },
  data() {
      return {
        // header nav menu 
        headerNavLinks: [
          {
              text: "Home",
              url: "#",
          },
          {
              text: "Culinary History",
              url: "#",
          },
          {
              text: "Our Team",
              url: "#",
          },
          {
              text: "Our Menu",
              url: "#",
          },
          {
              text: "Takeout",
              url: "#",
          },
          {
              text: "Bulletin",
              url: "#",
          },
          {
              text: "Reservation",
              url: "#",
          },
          {
              text: <i class="fas fa-shopping-cart"></i>,
              url: "#",
          }
        ]
      }
  }
}
</script>

<style lang="scss">
@import '~@fortawesome/fontawesome-free/css/all.min.css';

* {
  margin: 0;
  padding: 0;
  box-sizing: border-box;
}
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
}
</style>
