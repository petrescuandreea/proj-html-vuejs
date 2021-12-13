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
              badge: null,
              url: "#",
          },
          {
              text: "Culinary History",
              badge: null,
              url: "#",
          },
          {
              text: "Our Team",
              badge: null,
              url: "#",
          },
          {
              text: "Our Menu",
              badge: null,
              url: "#",
          },
          {
              text: "Takeout",
              badge: "New",
              url: "#",
          },
          {
              text: "Bulletin",
              badge: null,
              url: "#",
          },
          {
              text: "Reservations",
              badge: null,
              url: "#",
          },
          {
              icon: "fas fa-shopping-cart",
              badge: null,
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
