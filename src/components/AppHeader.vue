<template>
    <section>
        <div class="text-col">
            <!-- logo -->
            <img src="../assets/img/logo-restaurant.png" alt=" Avada restaurant logo">
            <!-- content  -->
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
                    <p>Pellentesque vitae viverra risus, sagitis. Venenatis ridiculus scelerisque nisi in urna nulla. Sit tempor a et nisl, ac felis.</p>
                    <!-- button  -->
                    <button>Explore the menu</button>
                    
                </div>
            </div>
        </div>

        <!-- image column  -->
        <div class="image-col">
            <div class="overlay">
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
    .text-col {
        width: 45%;
        height: 100%;
        float: left;
        color: #676059;
        background-color: rgba(3,3,3,255);
        padding: 40px 80px 0 80px;
    
        .content {
            margin: 110px 0;
    
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
                // margin: 0 50px 0 120px;
                margin-left: 120px;
    
                h1 {
                    font-size: 55px;
                    text-transform: uppercase;
                    color: white;
                    margin: 40px 0;
                }
    
                p {
                    line-height: 30px;
                    margin-bottom: 40px;
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

    .image-col {
        width: 55%;
        height: 100%;
        float: left;
        position: relative;
        background-image: url("../assets/img/slider52x.jpg");
        background-size: cover;

        .overlay {
            position: absolute;
            top: 0;
            right: 0;
            bottom: 0;
            left: 0;
            background-color: rgba(0, 0, 0, 0.2);

            .nav-container {
                position: absolute;
                top: 55px;
                width: 100%;
    
                ul {
                    display: flex;
                    justify-content: center;
                    list-style: none;

                    li {
                        margin-right: 28px;
    
                        a {
                            font-size: 12px;
                            color: #9c958f;
                            text-decoration: none;
                            font-weight: bold;

                            &.active {
                                color: white;
                            }

                            .new {
                                font-size: 10px;
                                padding: 2px 8px;
                                border: 1px solid white;
                                margin-left: 5px;
                            }
                        }
                    }
                }
            }
        }
    }
}
.section::after {
    content: "";
    display: table;
    clear: both;
}


</style>
