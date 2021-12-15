<template>
    <section id="takeout">
      <div class="clearfix">
          <!-- image column  -->
          <div class="image-col"></div>
          
          <!-- text column  -->
          <div class="text-col">
            <div class="content">
                <div class="content-top">
                    <!-- line  -->
                    <div class="line"></div>

                    <h3>enjoy your meal at home</h3>
                </div>

                <div class="content-bottom">
                    <!-- title  -->
                    <h1>takeout now available</h1>

                    <!-- text  -->
                    <div class="text-container">
                        <p>
                            Pellentesque vitae viverra risus, sagitis. Venenatis ridiculus scelerisque nisi in urna nulla non arcu moris tortor.
                        </p>
                    </div>

                    <!-- button  -->
                    <button>
                        <i class="fas fa-car"></i>
                        view takeout menu
                    </button>
                </div>
            </div>
          </div>
        </div>
    </section>
</template>

<script>
export default {
  name: 'Takeout',
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped lang="scss">
#takeout {
    height: 615px;

    .clearfix {
        height: 100%;

        .image-col {
            width: 55%;
            height: 100%;
            float: left;
            background-image: url("../assets/img/slider72x-scaled.jpg");
            background-size: cover;
            background-position: bottom;
        }

        .text-col {
            width: 45%;
            height: 100%;
            float: left;
            color: white;
            background-color: rgba(3,3,3,255);
            padding: 40px 80px 0 80px;
        
            .content {
                margin: 110px 0;
                color: #676059;
        
                .content-top {
                    display: flex;
                    align-items: center;
        
                    .line {
                        width: 60px;
                        border-bottom: 2px solid;
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
                        color:white;
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

                        i {
                            margin-right: 5px;
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
