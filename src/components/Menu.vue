<template>
    <section id="menu">
        <div class="cards">
            <div id="menu-hors" class="card">
                <div class="content">
                    <h2>
                        Hors d'oeuvres
                    </h2>

                    <div class="dish" v-for="dish, i in horsDishes" :key="i">
                        <div class="type">
                            <span class="name"> {{ dish.typeOfDish }} </span>
                            <span class="price"> &#36;{{ dish.price }} </span>
                        </div>

                        <div class="description">
                            <p>
                            {{ dish.description }}
                            </p>
                        </div>
                    </div>
                </div>
            </div>

            <div id="menu-main-course" class="card">
                <div class="content">
                    <h2>
                        Main course
                    </h2>

                    <div class="dish" v-for="dish, i in mainCourseDishes" :key="i">
                        <div class="type">
                            <span class="name"> {{ dish.typeOfDish }} </span>
                            <span class="price"> &#36;{{ dish.price }} </span>
                        </div>

                        <div class="description">
                            <p>
                                {{ dish.description }}
                            </p>
                        </div>
                    </div>
                </div>
            </div>

            <div id="menu-desserts" class="card">
                <div class="content">
                    <h2>
                        Desserts
                    </h2>

                    <div class="dish" v-for="dessert, i in desserts" :key="i">
                        <div class="type">
                            <span class="name"> {{ dessert.typeOfDessert }} </span>
                            <span class="price"> &#36;{{ dessert.price }} </span>
                        </div>

                        <div class="description">
                            <p>
                            {{ dessert.description }}
                            </p>
                        </div>
                    </div>
                </div>
            </div>
        </div>
    </section>
</template>

<script>
export default {
  name: 'Menu',
  data() {
      return {
          horsDishes: [
              {
                  typeOfDish: 'Ahi salmon nigiri',
                  price: 48,
                  description: 'Eget vulputate vitae quis rutrun blandit sed. Quam nulla sit lacinia.'
              },
              {
                  typeOfDish: 'Umi masu salad',
                  price: 21,
                  description: 'Molis ornare sit sapien, sodales. Cursus duis proin semper quisque.'
              },
              {
                  typeOfDish: 'Temaki with crab',
                  price: 32,
                  description: 'Ac vel, risus ornare senectus placerat duis amet dictumst tellus.'
              },
              {
                  typeOfDish: 'California rolls',
                  price: 22,
                  description: 'Ac vel, risus ornare senectus placerat duis amet dietumst tellus.'
              },
          ],

          mainCourseDishes: [
              {
                  typeOfDish: 'Braised abalone',
                  price: 52,
                  description: 'Molis ornare sit sapien, sodales. Cursus duis proin semper quisque.'
              },
              {
                  typeOfDish: 'Twice cooked pork',
                  price: 21,
                  description: 'Ac vel, risus ornare senectus placerat duis amet dictumst tellus.'
              },
              {
                  typeOfDish: 'Kung Pao Chicken',
                  price: 32,
                  description: 'Quis duis sit dictum aliquam a velit enim. Tellus in sit augue aliquam.'
              },
              {
                  typeOfDish: 'Char sui & sushis',
                  price: 48,
                  description: 'Feugiat rhoncus ipsum tristique purus diam, et dolor molestie.'
              },
          ],

           desserts: [
              {
                  typeOfDessert: 'Chocolate Ball Cacke',
                  price: 13,
                  description: 'In pellentesque in felis massa vehicula. In sed euismod ut.'
              },
              {
                  typeOfDessert: 'Lime Pie with Crust',
                  price: 14,
                  description: 'Molis ornare sit sapien, sodales. Cursus duis proin semper quisque.'
              },
              {
                  typeOfDessert: 'Rasberry Pear Cake',
                  price: 18,
                  description: 'Eget vulputate vitae quis rutrun blandit sed. Quam nulla sit.'
              },
              {
                  typeOfDessert: 'Café au lait',
                  price: 6,
                  description: 'Eget vulputate vitae quis rutrun blandit sed. Quam nulla sit.'
              },
          ],
      }
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped lang="scss">
#menu {
    padding: 105px 80px 80px 80px; 

    .cards {
        display: flex;
        flex-wrap: wrap;

        .card {
            width: calc(100% / 3);
            
            .content {
                padding: 80px 60px;

                h2 {
                    font-size: 30px;
                    margin-bottom: 40px;
                }


                h2, .name {
                    text-transform: uppercase;
                }

                .dish {
                    margin-bottom: 40px;

                    .type {
                        display: flex;
                        justify-content: space-between;
                        align-items: center;

                        .name {
                            font-size: 20px;
                            font-weight: bold;
                        }

                        .price {
                            font-size: 12px;
                        }
                    }

                    .description {
                        padding-top:15px;

                        p {
                            font-size: 15px;
                            line-height: 25px;
                        }
                    }
                }
            }
        }

        #menu-hors, #menu-desserts {
            background-color: rgba(232,232,232,255);
        }

        #menu-main-course {
            color: white;
            background-image: url("../assets/img/misc22x.jpg");
            background-size: cover;
            margin: -25px 0 25px 0;

            .content {
                background: linear-gradient(180deg, black, rgba(0, 0, 0, 0.2));
            }
            
        }
    }

}
</style>
