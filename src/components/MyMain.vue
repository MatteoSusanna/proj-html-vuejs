<template>
  <main>
    <SectionWelcome />

    <SectionOverview />

    <SectionSlider />

    <SectionClasse />

    <SectionEducation />

    <SectionImg />

    <SectionMeet />

    <SectionSlider2 />

    <SectionWhat />

    <SectionMap />

    <SectionContact />
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
import SectionSlider2 from './SectionSlider2.vue'
import SectionWhat from './SectionWhat.vue'
import SectionMap from './SectionMap.vue'
import SectionContact from './SectionContact.vue'

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
      SectionSlider2,
      SectionWhat,
      SectionMap,
      SectionContact,
    },
}
</script>

<style lang="scss">
@import '../style/general.scss';
</style>