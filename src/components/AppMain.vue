<template>
    <div>
        <CaliforniaRollsProduct/>
        <AppSection2/>
        <AppSection3/>
    </div>
</template>

<script>

import CaliforniaRollsProduct from '@/components/CaliforniaRollsProduct.vue';
import AppSection2 from '@/components/AppSection2.vue';
import AppSection3 from '@/components/AppSection3.vue';

export default {
  name: 'AppMain',
  components: {
    CaliforniaRollsProduct,
    AppSection2,
    AppSection3,
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped lang="scss">

</style>
