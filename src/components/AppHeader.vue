<template>
    <section>
        <!-- <div class="clearfix"> -->
            <!-- text column  -->
            <div class="text-col">
                <!-- logo -->
                <img src="../assets/img/logo-restaurant.png" alt=" Avada restaurant logo">

                <!-- content  -->
                <div class="content">
                    <div class="content-top">
                        <!-- line  -->
                        <div class="line"></div>

                        <h3>The best table in town</h3>
                    </div>

                    <div class="content-bottom">
                        <!-- title  -->
                        <h1>Fine dining experience</h1>

                        <!-- text  -->
                        <p>Pellentesque vitae viverra risus, sagitis. Venenatis ridiculus scelerisque nisi in urna nulla. Sit tempor a et nisl, ac felis.</p>

                        <!-- button  -->
                        <div class="btn bg-white">Explore the menu</div>
                        
                    </div>
                </div>
            </div>

            <!-- image column  -->
            <div class="image-col">
                <img src="../assets/img/slider52x.jpg" alt="">
                <!-- nav menu  -->
                <!-- <nav>
                    <ul>
                        <li><a href="#"></a></li>
                    </ul>
                </nav> -->

            </div>
        <!-- </div> -->
    </section>
</template>

<script>
export default {
  name: 'AppHeader',
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped lang="scss">
section {
    height: 715px;

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
                // margin: 0 50px 0 120px;
                margin-left: 120px;
    
                h1 {
                    font-size: 55px;
                    text-transform: uppercase;
                    margin: 40px 0;
                }
    
                p {
                    line-height: 30px;
                    margin-bottom: 40px;
                }
    
                .btn {
                    text-transform: uppercase;
                    font-size: 12px;
                    border: 1px solid white;
                    padding: 10px 30px;
                    display: inline;
                    cursor: pointer;
    
                    &.bg-white:hover{
                        color: black;
                        background-color: white;
                    }
                }
            }
        }
    }

    .image-col {
        width: 55%;
        height: 100%;
        float: left;
    
        img {
            width: 100%;
            height: 100%;
            object-fit: cover;
        }
    }
}

.section::after {
    content: "";
    display: table;
    clear: both;
}


</style>
