<template>
    <section id="team">
        <div class="center-container">
            <div id="title">
                <h2>
                    What critics are saying about us
                </h2>

                <!-- line  -->
                <div class="line-title"></div>
            </div>

            <div class="extend-card">
                <!-- image column  -->
                <div class="image-col">
                    <img src="../assets/img/blog72x-600x687.jpg" alt="team member's image">
                </div>

                <!-- text column  -->
                <div class="text-col">
                    <!-- member name  -->
                    <span>meggy stewart</span>

                    <!-- daily newspaper name  -->
                    <h3>new york times</h3>

                    <!-- stars  -->
                    <div class="stars">
                        <i class="fas fa-star"></i>
                        <i class="fas fa-star"></i>
                        <i class="fas fa-star"></i>
                        <i class="fas fa-star"></i>
                        <i class="fas fa-star"></i>
                    </div>

                    <!-- line  -->
                    <div class="line"></div>

                    <!-- text  -->
                    <div class="text">
                        <p>
                            Non arcu mauris tortor ultrices mollis tellus euismod fermentum. Habitant amet tincidunt id sapien accumsan sed at.
                        </p>

                        <p>
                            Mmalesuada ullamcorper amet. Pertium pertium dignissim nisi.
                        </p>
                    </div>

                    <!-- button  -->
                    <button>
                        read full article
                    </button>
                </div>
            </div>

            <!-- team cards  -->
            <div class="cards">
                <div class="card" v-for="card, i in cards" :key="i">
                    <div class="card-bg">
                        <img :src="require(`../assets/img/${card.image}`)" :alt="card.name">
                    </div>

                    <div class="text">
                        <!-- member name  -->
                        <span>{{ card.name }}</span>

                        <!-- daily newspaper name  -->
                        <h3>{{ card.dailyNewspaper }}</h3>

                        <!-- stars  -->
                        <div class="stars">
                            <i :class="card.star"></i>
                            <i :class="card.star"></i>
                            <i :class="card.star"></i>
                            <i :class="card.star"></i>
                            <i :class="card.star"></i>
                        </div>

                        <!-- line  -->
                        <div class="line"></div>

                        <!-- text  -->
                        <p>
                            {{ card.text }}
                        </p>

                        <!-- button  -->
                        <button>
                            {{ card.button }}
                        </button>
                    </div>
                </div>
            </div>
        </div>

    </section>
</template>

<script>
export default {
  name: 'Team',
  data() {
      return {
          cards: [
              {
                  image:'info52x.jpg',
                  name: 'mary maxey',
                  dailyNewspaper: 'the guardian',
                  star:'fas fa-star',
                  line: '',
                  text: 'Non arcu mauris tortor ultrices mollis tellus eusimod fermentum. Habitant amet tincidunt id sapien accumsan sed.',
                  button: 'read full article'
              },
              {
                  image:'info12x.jpg',
                  name: 'patrick monroe',
                  dailyNewspaper: 'globe and mail',
                  star:'fas fa-star',
                  line: '',
                  text: 'Vivamus magna justo, lacinia eget consectetur sed,convallis at tellus. Nulla porttitor accumsan tincidunt.',
                  button: 'read full article'
              },
          ]
      }
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped lang="scss">
#team {
    padding: 80px 0; 

    .center-container {
        width: 75%;
        margin: 0 auto;

        h2 {
            text-align: center;
            font-style: italic;
            font-weight: normal;
            margin-bottom: 20px;
        }

        .line-title {
            width: 40px;
            border-bottom: 1px solid #dadada;
            margin:0 auto 40px auto;
        }

        // general rules 
        span {
            font-size: 12px;
        }

        h3 {
            font-size: 30px;
            color: white;;
        }

        .stars {
            i {
                margin-right: 5px;
                color: white;;
            }
        }

        .line {
            width: 60px;
            border-bottom: 1px solid #676059;
            margin-left: 0;
        }

        p {
            font-size: 15px;
            line-height: 25px;
            padding-bottom: 20px;
        }

        button {
            font-size: 12px;
            border: 1px solid white;
            background-color: black;
            color: white;
            padding: 10px 30px;
            cursor: pointer;
            margin-top: 20px;

            &:hover{
                color: black;
                background-color: white;
            }
        }

        .stars, h3 {
            margin: 30px 0;
        }

        span, h3, button {
            text-transform: uppercase;
        }

        .extend-card {
            height: 650px;

            .image-col {
                width: 50%;
                height: 100%;
                float: left;

                img {
                    width: 100%;
                    height: 100%;
                }
            }

            .text-col {
                width: 50%;
                height: 100%;
                float: left;
                background-color: black;
                color: #676059;
                padding: 110px;
                cursor: pointer;
                transition: all;

                &:hover {
                    transform: scale(1.05);
                }

                .text {
                    max-height: 170px;
                    overflow: hidden;
                }

            }
        }

        .extend-card::after {
            content: "";
            display: table;
            clear: both;
        }


        .cards {
            display: flex;
            flex-wrap: wrap;
            justify-content: space-between;
            margin: 40px 0;

            .card {
                width: 45% ;
                height: 600px;
                position: relative;
                color: #676059;
                

                .card-bg , img {
                    width: 100%;
                    height: 100%;
                }

                .text {
                    width: 100%;
                    height: 100%;
                    position: absolute;
                    top: 0;
                    left: 0;
                    padding: 100px;
                    background: linear-gradient(180deg, black, rgba(0, 0, 0, 0.2));

                    p {
                        max-height: 80px;
                        overflow: hidden;
                    }

                    button {
                        background-color: transparent;

                        &:hover {
                            background-color: white;
                        }
                    }
                }

            }
        }
    }
}


</style>
