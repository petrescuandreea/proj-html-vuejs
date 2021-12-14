<template>
    <ul id="sm-channels">
        <!-- con un ciclo vado a stampare tutti gli oggetti contenuti nell'array smChannels presente nel componente padre AppFooter -->
        <li v-for="channel, i in channels" :key="i">
            <a :href="channel.url">
                <i :class="channel.icon"></i>
            </a>
        </li>
    </ul>
</template>

<script>
export default {
  name: 'SocialMediaChannels',
  props: {
    //   ricevo le info dei canali social dal componente padre AppFooter 
      channels: Array,
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped lang="scss">
#sm-channels {
    ul {
        margin: 40px 0;

        li {
            display: inline;

            a {
                cursor: pointer;
                padding: 10px 15px;
                background-color: white;
                border-radius: 50%;
                text-align: center;
                margin: 0 5px;

                &:hover {
                    background-color: darkgray;

                    i {
                        color: blue
                    }
                }

                i {
                    color: black;
                }
            }
        }
    }
}

</style>