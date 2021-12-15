<template>
  <section id="bulletin">
      <div class="center-container">
          <h2>Latest news &#38; promotions</h2>

          <div class="line"></div>

          <div class="cards-container">
                <!-- da stampare dinamicamente  -->
                <div class="card" v-for="card, i in cards" :key="i">
                    <div class="show">
                        <div class="card-img">
                            <img :src="require(`../assets/img/${card.image}`)" alt="image">
                        </div>

                        <div class="card-text">
                            <h3>
                                {{ card.title }}
                            </h3>


                            <p>
                                {{ card.info }}
                            </p>
                        </div>
                    </div>

                    <div class="hidden">
                        <div class="content">
                            <div class="card-img">
                                <img :src="require(`../assets/img/${card.image}`)" alt="image">
                            </div>

                            <div class="hidden-text">
                                <i :class="card.icon"></i>
                                <h3>
                                    {{ card.title }}
                                </h3>
                                <span>
                                    {{ card.new }}
                                </span>
                            </div>
                        </div>
                    </div>
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
                  image:'blog92x-400x458.jpg',
                  title:'the best coffee in town',
                  info:'By admin | January 7th, 2020 | Categories: News',
                  icon: 'fas fa-link',
                  new: 'News'
              },
              {
                  image:'blog72x-400x458.jpg',
                  title:'discover our new menu',
                  info:'By admin | January 7th, 2020 | Categories: News',
                  icon: 'fas fa-link',
                  new: 'News'
              },
              {
                  image:'blog82x-400x458.jpg',
                  title:'we now accept square!',
                  info:'By admin | January 7th, 2020 | Categories: News',
                  icon: 'fas fa-link',
                  new: 'News'
              },
          ]
      }
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped lang="scss">
#bulletin {
    padding: 80px 0; 

    .center-container {
        width: 75%;
        margin: 0 auto;
        text-align: center;

        h2 {
            font-style: italic;
            font-weight: normal;
            margin-bottom: 20px;
        }

        .line {
            width: 40px;
            border-bottom: 1px solid #dadada;
            margin: 0 auto 40px auto;
        }

        .cards-container {
            display: flex;
            flex-wrap: wrap;
            justify-content: space-between;

            .card {
                width: calc(95% / 3);
                position: relative;
                cursor: pointer;

                img {
                    width: 100%;
                    display: block;
                }

                .card-text {
                    h3 {
                        font-size: 18px;
                        text-transform: uppercase;
                        margin: 30px 0 10px 0;
                    }

                    p {
                        font-size: 12px;
                    }
                }

                .hidden {
                    position: absolute;
                    top: 0;
                    left: 0;
                    display: none;

                    .content {
                        position: relative;
                        .hidden-text {
                            width: 100%;
                            height: 100%;
                            color: #d6cbbd;
                            position: absolute;
                            top: 0;
                            left: 0;
                            background: linear-gradient(180deg, black, rgba(0, 0, 0, 0.2));
                            display: flex;
                            flex-direction: column;
                            justify-content: center;
                            

                            i, span {
                                font-size: 12px;
                            }

                            h3 {
                                text-transform: uppercase;
                                margin: 15px 0;
                            }
                        }
                    }


                }

                &:hover .hidden {
                    display: block;
                }

                &:hover .show {
                    display: none;
                }
            }
        }
    }
}

</style>
