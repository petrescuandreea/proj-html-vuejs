<template>
    <section>
        <!-- header navigation bar  -->
        <div id="header-nav" class="clearfix">
            <!-- logo  -->
            <div id="logo">
                <img src="../assets/img/logo-restaurant.png" alt=" Avada restaurant logo">
            </div>

            <!-- nav menu  -->
            <div class="nav-container">
                    <nav>
                        <ul>
                            <li v-for="link, i in links" :key="i">
                                <a v-if="link.icon" :href="link.url">
                                    <i :class="link.icon"></i> 
                                </a>
                                <a v-else :href="link.url" :class="link.here ? 'active' : ''">
                                    {{ link.text }} 
                                    
                                    <span class="new" v-if="link.badge">
                                        {{ link.badge }}
                                    </span>
                                </a>
                            </li>
                        </ul>
                    </nav>
                </div>
        </div>


        <!-- jumbo  -->
        <div id="jumbo-container" class="clearfix">
            <!-- text column  -->
            <div class="text-col">
                <div class="content">
                    <div class="content-top">
                        <!-- line  -->
                        <div class="line"></div>

                        <h3>The best table in town </h3>
                    </div>

                    <div class="content-bottom">
                        <!-- title  -->
                        <h1>Fine dining experience</h1>

                        <!-- text  -->
                        <div class="text-container">
                            <p>
                                Pellentesque vitae viverra risus, sagitis. Venenatis ridiculus scelerisque nisi in urna nulla. Sit tempor a et nisl, ac felis.
                            </p>
                        </div>

                        <!-- button  -->
                        <div class="btn bg-white">Explore the menu</div>
                        
                    </div>
                </div>
            </div>

            <!-- image column  -->
            <div class="image-col">
                <div class="overlay"></div>
            </div>
        </div>
    </section>
</template>

<script>

export default {
  name: 'AppHeader',
  props: {
      links: Array,
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped lang="scss">
section {
    height: 715px;
    position: relative;

    #header-nav {
        width: 95%;
        margin: 0 auto;
        padding: 20px 0;
        line-height: 80px;
        z-index: 1;

        #logo {
            float: left;

            img {
                line-height: 80px;
                vertical-align: middle;
                margin-left: 45px;
            }
        }

        .nav-container {
            float: right;

            nav {
                margin-right: 15px;

                ul {

                    li {
                        display: inline-block;
                        margin-right: 18px;

                        a {
                            font-size: 15px;
                            color: #9c958f;
                            text-decoration: none;
                            font-weight: bold;

                            .new {
                                line-height: 80px;
                                vertical-align: middle;
                                font-size: 10px;
                                padding: 2px 8px;
                                border: 1px solid white;
                                margin-left: 5px;
                            }

                            &.active {
                                color: white;
                            }
                        }
                    }
                }
            }
        
        }
    }

    #jumbo-container {
        width: 100%;
        height: 100%;
        position: absolute;
        top: 0;
        left: 0;
        z-index: -1;

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
                        font-size: 55px;
                        text-transform: uppercase;
                        line-height: 75px;
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
            background-image: url("../assets/img/slider52x.jpg");
            background-size: cover;

            .overlay {
                position: absolute;
                top: 0;
                right: 0;
                bottom: 0;
                left: 0;
                background-color: rgba(0, 0, 0, 0.2);
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
