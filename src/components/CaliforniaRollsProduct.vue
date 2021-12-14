<template>
  <section id="california-rolls">
      <div class="center-container">
        <!-- text column  -->
        <div class="text-col">
            <div class="content">
                <p>
                    <span>hac tellus, felis risus at</span>
                    mattis mattis. Eget euismod semper eget tortor, donee amet, blandit. Tristique facilisi faucibus elementum feugiat in nam in feugiat. Ipsum odio etiam duis facilisis amet vulputate.
                </p>

                <h2>
                    food is our common ground, a universal experience.
                </h2>

                <p>
                    Tristique tempus condimentum diam donee. Condimentum ullamcorper sit elementum hendrerit mi nulla in consequat, ut. Metus, nullam seelerisque netus viverra dui.
                </p>

                <img src="../assets/img/signature.jpg" alt="signature">
            </div>
        </div>

        <!-- image column  -->
        <div class="image-col">
            <img src="../assets/img/info22x.jpg" alt="California Rolls image">
            <span>
                california rolls - &#65129;22
            </span>
        </div>

      </div>
  </section>
</template>

<script>
export default {
  name: 'CaliforniaRollsProduct',
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped lang="scss">
#california-rolls {
    padding: 80px 0;

    .center-container {
        width: 75%;
        margin: 0 auto;

        .text-col {
            width: 60%;
            float: left;
            padding: 40px 80px 0 0;

            p {
                color: #676059;
                width: 90%;
                line-height: 25px;

                span {
                    color: black;
                    text-transform: uppercase;
                    font-weight: bold;
                }
            }

            h2 {
                width: 75%;
                font-size: 38px;
                font-weight: bold;
                text-transform: uppercase;
                line-height: 50px;
                margin: 45px 0;
            }

            img {
                width: 20%;
                margin-top: 20px;
            }
        }

        .image-col {
            width: 40%;
            float: left;
            position: relative;

            img {
                width: 100%;
                cursor: pointer;

                &:hover {
                    box-shadow: 0 1px 5px black;
                }
            }

            span {
                font-size: 12px;
                color: white;
                text-transform: uppercase;
                position: absolute;
                bottom: 45px;
                left: 145px;
            }
        }

    }

    .center-container::after {
        content: "";
        display: table;
        clear: both;
    }
}
</style>
