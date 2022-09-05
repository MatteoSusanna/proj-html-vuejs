<template>
  <main>
    <SectionWelcome />

    <SectionOverview />

    <SectionSlider />

  </main>
  

</template>

<script>
import SectionWelcome from './SectionWelcome.vue'
import SectionOverview from './SectionOverview.vue'
import SectionSlider from './SectionSlider.vue'

export default {
    nome: 'MyMain',
    components:{
      SectionWelcome,
      SectionOverview,
      SectionSlider,
    },
}
</script>

<style lang="scss">
@import '../style/general.scss';




</style>