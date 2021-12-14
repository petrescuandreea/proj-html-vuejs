<template>
  <section id="reservations">
      <div class="center-container">
          <div class="card" v-for="card, i in cards" :key="i">
              <img :src="require(`../assets/img/${card.image}`)" :alt="card.info">

              <h3>
                  {{ card.title }}
              </h3>

              <div>
                  {{ card.line }}
              </div>

              <p>
                  {{ card.text }}
              </p>

              <div class="btn">
                  {{ card.button }}
              </div>
          </div>

      </div>

  </section>
</template>

<script>
export default {
  name: 'AppSection2',
  data() {
      return {
          cards: [
              {
                  image: 'sushi-1.png',
                  info: 'sushi image',
                  title: 'the best table in town',
                  line: '',
                  text: 'Sed aaeneam egestas ut aliquam turpis mauris, molestie. Vitae tellus tempor sem id tempus neque, tellus turpis turpis. Morbi tortor id gravida aliquet.',
                  button: 'explore the menu'
              },
              {
                  image: 'sushi-2.png',
                  info: 'sushi image',
                  title: 'perfect for groups',
                  line: '',
                  text: 'Qua eu proin sit massa condimentum. Volutpat non pulvinar aliquet nunc. Orci elementum in aliquet a gravida vivamus aliquam turpis vitae-',
                  button: 'make a reservation'
              },
              {
                  image: 'sushi-3.png',
                  info: 'sushi image',
                  title: 'fresh produce everyday',
                  line: '',
                  text: 'Hendreit amet, volutpat leo non, commodo maecenas scelerisque tincidunt. Morbi vulputate morbi purus quisque sit sagittis orci elementum gravida.',
                  button: 'learn more about us'
              }
          ]
      }
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped lang="scss">


</style>
