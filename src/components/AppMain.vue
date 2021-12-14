<template>
    <div>
        <CaliforniaRollsProduct/>
        <Reservations/>
        <AppSection3/>
    </div>
</template>

<script>

import CaliforniaRollsProduct from '@/components/CaliforniaRollsProduct.vue';
import Reservations from '@/components/Reservations.vue';
import AppSection3 from '@/components/AppSection3.vue';

export default {
  name: 'AppMain',
  components: {
    CaliforniaRollsProduct,
    Reservations,
    AppSection3,
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped lang="scss">

</style>
