<template>
    <div>
        <CaliforniaRollsProduct/>
        <Reservations/>
        <CulinaryHistory/>
        <Team/>
        <KungPaoChicken/>
        <Bulletin/>
        <Takeout/>
        <Menu/>
    </div>
</template>

<script>

import CaliforniaRollsProduct from '@/components/CaliforniaRollsProduct.vue';
import Reservations from '@/components/Reservations.vue';
import CulinaryHistory from '@/components/CulinaryHistory.vue';
import Team from '@/components/Team.vue';
import KungPaoChicken from '@/components/KungPaoChicken.vue';
import Bulletin from '@/components/Bulletin.vue';
import Takeout from '@/components/Takeout.vue';
import Menu from '@/components/Menu.vue';

export default {
  name: 'AppMain',
  components: {
    CaliforniaRollsProduct,
    Reservations,
    CulinaryHistory,
    Team,
    KungPaoChicken,
    Bulletin,
    Takeout,
    Menu,
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped lang="scss">

</style>
