<template>
  <section id="reservations">
      <div class="center-container">
          <div class="card" v-for="card, i in cards" :key="i">
              <img :src="require(`../assets/img/${card.image}`)" :alt="card.info">

              <h3>
                  {{ card.title }}
              </h3>

              <div class="line">
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
                  text: 'Qua eu proin sit massa condimentum. Volutpat non pulvinar aliquet nunc. Orci elementum in aliquet a gravida vivamus aliquam turpis vitae.',
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
#reservations {
    padding: 80px 0;
    
    .center-container {
        width: 75%;
        margin: 0 auto;
        display: flex;
        flex-wrap: wrap;
        justify-content: center;

        .card {
            width: calc(85% / 3);
            margin-right: 5%;
            margin-bottom: 70px;
            text-align: center;

            h3 {
                text-transform: uppercase;
                margin: 30px 0;
            }

            .line {
                width: 80px;
                border-bottom: 1px solid #dadada;
                margin: 0 auto 30px auto;
            }

            p {
                color: #676059;
                line-height: 25px;
                margin-bottom: 40px;
            }

            .btn {
                text-transform: uppercase;
                font-size: 12px;
                border: 1px solid #dadada;
                padding: 10px 30px;
                display: inline;
                cursor: pointer;

                &:hover {
                    border-color: black;
                }
            }
        }
    }
}


</style>
