<template>
    <div>
        <AppSection1/>
        <AppSection2/>
    </div>
</template>

<script>

import AppSection1 from '@/components/AppSection1.vue';
import AppSection2 from '@/components/AppSection2.vue';

export default {
  name: 'AppMain',
  components: {
    AppSection1,
    AppSection2,
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped lang="scss">

</style>
