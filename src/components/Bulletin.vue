<template>
  <section id="bulletin">
      <div class="center-container">
          <h2></h2>

          <div class="line"></div>

          <!-- da stampare dinamicamente  -->
          <div class="card">
              <div class="card-img">
                  <img src="" alt="">
              </div>

              <div class="card-text">
                  <h3>
                      
                  </h3>


                  <p>

                  </p>
              </div>
          </div>
      </div>

  </section>
</template>

<script>
export default {
  name: 'Bulletin',
  data() {
      return {
          cards: [
              {
                  image:'blog92x-400x458',
                  title:'the best coffee in town',
                  info:'By admin | January 7th, 2020 | Categories: News'
              },
              {
                  image:'blog72x-400x458',
                  title:'discover our new menu',
                  info:'By admin | January 7th, 2020 | Categories: News'
              },
              {
                  image:'blog82x-400x458',
                  title:'we now accept square!',
                  info:'By admin | January 7th, 2020 | Categories: News'
              },
          ]
      }
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped lang="scss">

</style>
