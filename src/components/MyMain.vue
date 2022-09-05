<template>
  <main>
    <SectionWelcome />

    <SectionOverview />

    <SectionSlider />

    <SectionClasse />

    <SectionEducation />

    <SectionImg />

    <SectionMeet />
  </main>
  

</template>

<script>
import SectionWelcome from './SectionWelcome.vue'
import SectionOverview from './SectionOverview.vue'
import SectionSlider from './SectionSlider.vue'
import SectionClasse from './SectionClasse.vue'
import SectionEducation from './SectionEducation.vue'
import SectionImg from './SectionImg.vue'
import SectionMeet from './SectionMeet.vue'

export default {
    nome: 'MyMain',
    components:{
      SectionWelcome,
      SectionOverview,
      SectionSlider,
      SectionClasse,
      SectionEducation,
      SectionImg,
      SectionMeet,
    },
}
</script>

<style lang="scss">
@import '../style/general.scss';




</style>