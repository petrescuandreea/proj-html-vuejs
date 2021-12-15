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
    height: 700px;
    background-image: url("../assets/img/hero42x.jpg");
    background-size: cover;
    background-position: center;
}

</style>
