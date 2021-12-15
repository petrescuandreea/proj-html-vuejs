<template>
    <section id="braised-abalone-product">
        <div class="content-container">
            <!-- title  -->
            <div class="title">
                <h2>Braised Abalone</h2>
                <span class="price">
                    &#36;52
                </span>
            </div>

            <!-- line  -->
            <div class="line"></div>

            <!-- text  -->
            <div class="text">
                <p>
                    Pretium accumsan porttitor viverra leo gravida mollis imperdiet. Fringilla nibh pharetra sociis leo amet.
                </p>
            </div>

            <!-- button  -->
            <button>
                View in the menu
            </button>
        </div>
    </section>
</template>

<script>
export default {
  name: 'BraisedProduct',
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped lang="scss">
#braised-abalone-product {
    background-image: url("../assets/img/hero42x.jpg");
    background-size: cover;
    background-position: center;
    padding: 80px 0 80px 200px;

    .content-container {
        background-color: black;
        color: #676059;
        width: 30%;
        padding: 80px 60px;

        .title {
            display: flex;
            justify-content: space-between;
            align-items: flex-start;
            color: white;

            h2 {
                font-size: 38px;
                text-transform: uppercase;
                line-height: 50px;
                width: 50%;
                margin-bottom: 60px;
            }
        }

        .line {
            width: 60px;
            border-bottom: 2px solid;
            margin-right: 60px;
            margin-bottom: 40px;
        }

        .text {
            max-height: 150px;
            overflow: hidden;
        }

        button {
            text-transform: uppercase;
            font-size: 12px;
            border: 1px solid white;
            background-color: black;
            color: white;
            padding: 10px 30px;
            margin-top: 40px;
            cursor: pointer;

            &:hover{
                color: black;
                background-color: white;
            }
        }

    }
}

</style>
