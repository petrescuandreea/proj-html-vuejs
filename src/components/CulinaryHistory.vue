<template>
  <section id="culinary-history">
      <div class="clearfix">
          <!-- image column  -->
          <div class="image-col"></div>
          
          <!-- text column  -->
          <div class="text-col">
            <div class="content">
                <div class="content-top">
                    <!-- line  -->
                    <div class="line"></div>

                    <h3>fine dining experience</h3>
                </div>

                <div class="content-bottom">
                    <!-- title  -->
                    <h1>the best table in town</h1>

                    <!-- text  -->
                    <div class="text-container">
                        <p>
                            Pellentesque vitae viverra risus, sagitis. Venenatis ridiculus scelerisque nisi in urna nulla.
                        </p>
                    </div>

                    <!-- button  -->
                    <button>Explore the menu</button>
                </div>
            </div>
          </div>
        </div>

  </section>
</template>

<script>
export default {
  name: 'CulinaryHistory',
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped lang="scss">
#culinary-history {
    height: 615px;

    .clearfix {
        height: 100%;

        .image-col {
            width: 55%;
            height: 100%;
            float: left;
            background-image: url("../assets/img/slider32x.jpg");
            background-size: cover;
            background-position: top;
        }

        .text-col {
            width: 45%;
            height: 100%;
            float: left;
            color: white;
            background-color: rgba(3,3,3,255);
            padding: 40px 80px 0 80px;
        
            .content {
                margin: 120px 0;
        
                .content-top {
                    display: flex;
                    align-items: center;
        
                    .line {
                        width: 60px;
                        border-bottom: 2px solid white;
                        margin-right: 60px;
                    }
        
                    h3 {
                        font-size: 15px;
                        font-weight: normal;
                        text-transform: uppercase;
                    }
                }
        
                .content-bottom {
                    margin-left: 120px;
        
                    h1 {
                        font-size: 38px;
                        text-transform: uppercase;
                        line-height: 50px;
                        margin: 40px 0;
                    }

                    .text-container {
                        max-height: 150px;
                        overflow-y: auto;
                        margin-bottom: 20px;

                        p {
                            line-height: 30px;
                            margin-bottom: 40px;
                        }
                    }
        
                    button {
                        text-transform: uppercase;
                        font-size: 12px;
                        border: 1px solid white;
                        background-color: black;
                        color: white;
                        padding: 10px 30px;
                        display: inline;
                        cursor: pointer;
        
                        &:hover{
                            color: black;
                            background-color: white;
                        }
                    }
                }
            }
        }
    }

    .clearfix::after {
        content: "";
        display: table;
        clear: both;
    }

}
</style>