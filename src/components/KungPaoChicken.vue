<template>
  <section id="kung-pao-chicken">
      <span>kung pao chicken - &#65129;32</span>
  </section>
</template>

<script>
export default {
  name: 'KungPaoChicken',
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped lang="scss">
#kung-pao-chicken {
    height: 500px;
    background-image: url("../assets/img/page52x.jpg");
    background-size: cover;
    position: relative;
    text-align: center;

    span {
        font-size: 12px;
        font-weight: bold;
        text-transform: uppercase;
        color: white;
        position: absolute;
        bottom: 15px;
    }
}
</style>