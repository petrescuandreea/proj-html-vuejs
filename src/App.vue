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
              here: true,
          },
          {
              text: "Culinary History",
              badge: null,
              url: "#",
              here: false,
          },
          {
              text: "Our Team",
              badge: null,
              url: "#",
              here: false,
          },
          {
              text: "Our Menu",
              badge: null,
              url: "#",
              here: false,
          },
          {
              text: "Takeout",
              badge: "New",
              url: "#",
              here: false,
          },
          {
              text: "Bulletin",
              badge: null,
              url: "#",
              here: false,
          },
          {
              text: "Reservations",
              badge: null,
              url: "#",
              here: false,
          },
          {
              icon: "fas fa-shopping-cart",
              badge: null,
              url: "#",
              here: false,
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
