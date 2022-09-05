<template>
  <main>
    <SectionWelcome />

    <SectionOverview />

  </main>
  

</template>

<script>
import SectionWelcome from './SectionWelcome.vue'
import SectionOverview from './SectionOverview.vue'

export default {
    nome: 'MyMain',
    components:{
      SectionWelcome,
      SectionOverview,
    },
}
</script>

<style lang="scss">
@import '../style/general.scss';




</style>