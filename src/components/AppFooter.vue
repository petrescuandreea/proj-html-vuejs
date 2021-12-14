<template>
    <div id="footer">
      <!-- text  -->
      <div id="footer-text">
        <div class="content">
          <!-- logo  -->
          <img src="../assets/img/logo-restaurant.png" alt="Avada restaurant logo">

          <!-- text  -->
          <p>
            Quam eu proin sit massa condimentum. Volutpat non pulvinar aliquet nunc. Quam eu porin sit massa contimentum.
          </p>

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
  data() {
      return {
        // creo array di oggetti con le info utili dei canali social che saranno inviate al componente figlio tramite prop 
         socialMediaChannels: [
              {
                  url: '#',
                  icon: 'fab fa-facebook-f',
                  alt: 'facebook logo'
              },
              {
                  url: '#',
                  icon: 'fab fa-twitter',
                  alt: 'twitter logo'
              },
              {
                  url: '#',
                  icon: 'fab fa-youtube',
                  alt: 'youtube logo'
              },
              {
                  url: '#',
                  icon: 'fab fa-instagram',
                  alt: 'instagram logo'
              },
              {
                  url: '#',
                  icon: 'fab fa-linkedin-in',
                  alt: 'linkedin logo'
              }
          ]
      }
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped lang="scss">
#footer {

  #footer-text {
    height: 500px;
    background-image: url("../assets/img/footer2x.jpg");
    background-size: cover;
    background-position: center;
    display: flex;
    align-items: center;

    .content {
      width: 30%;
      margin: 0 auto;
      text-align: center;

      img {
        margin: 20px 0;
      }

      p {
        color: #857f7c;
        line-height: 25px;
      }
    }
  }

  #copyright {
    text-align: center;
    padding: 30px 0;
    background-color: rgba(3,3,3,255);

    span {
      font-size: 10px;
      color: white;
    }
  }
}

</style>
