<template>
  <main>
    <SectionWelcome />

    <SectionOverview />

    <SectionSlider />

    <SectionClasse />

  </main>
  

</template>

<script>
import SectionWelcome from './SectionWelcome.vue'
import SectionOverview from './SectionOverview.vue'
import SectionSlider from './SectionSlider.vue'
import SectionClasse from './SectionClasse.vue'

export default {
    nome: 'MyMain',
    components:{
      SectionWelcome,
      SectionOverview,
      SectionSlider,
      SectionClasse,
    },
}
</script>

<style lang="scss">
@import '../style/general.scss';




</style>