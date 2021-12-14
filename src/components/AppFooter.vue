<template>
    <div id="footer">
      <!-- text  -->
      <div id="footer-text">
        <div class="content">
          <!-- logo  -->
          <img src="../assets/img/logo-restaurant.png" alt="Avada restaurant logo">

          <!-- text  -->
          <p></p>

          <!-- social media channels -->
          <div id="sm-channels">

          </div>

        </div>
      </div>

      <!-- copyright  -->
      <div id="copyright">
        <span>
          Copyright 2012 - 2019 Avada | All Rights Reserved | Powered by WordPress | ThemeFusion
        </span>
      </div>

    </div>
</template>

<script>
export default {
  name: 'AppFooter',
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped lang="scss">
#footer {

  #copyright {
    text-align: center;
    padding: 30px 0;
    background-color: rgba(3,3,3,255);

    span {
      font-size: 15px;
      color: white;
    }
  }
}

</style>
