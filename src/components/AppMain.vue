<template>
    <div>
        <CaliforniaRollsProduct/>
        <Reservations/>
        <CulinaryHistory/>
        <Team/>
    </div>
</template>

<script>

import CaliforniaRollsProduct from '@/components/CaliforniaRollsProduct.vue';
import Reservations from '@/components/Reservations.vue';
import CulinaryHistory from '@/components/CulinaryHistory.vue';
import Team from '@/components/Team.vue';

export default {
  name: 'AppMain',
  components: {
    CaliforniaRollsProduct,
    Reservations,
    CulinaryHistory,
    Team,
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped lang="scss">

</style>
