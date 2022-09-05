<template>
    <section id="welcome">
        <div class="text-center">

            <h2 class="pt">Welcome to Fable</h2>
            <p class="ptb">Fable daycare, preschool, and kindergerten</p>
            <img src="../assets/img/header_divider.png" alt="divisore">

            <div class="row">
            <div class="card pt pb" v-for="(card, indice) in welcomeArray" 
                :key='indice'>
                <div class="wrapper-img" :class="(card.bg?'bg-orange':'bg-butterflu')">
                <img :src="card.url" :alt="card.titolo">
                </div>
                <h4 class="ptb">{{card.titolo}}</h4>
                <p>{{card.descrizione}}</p>
            </div>
            </div>
        
      </div> 
    </section>
</template>

<script>
export default {
    nome: 'SectionWelcome',
    data(){
      return{
        welcomeArray: [
                        {
                          'url': require('../assets/img/schoolbag_alt.png'),
                          'titolo': 'Morbi Etos',
                          'bg': true,
                          'descrizione': 'Praesent interdum est gravida vehicula est node maecenas loareet morbi a dpsos òictis mpvi, est praesent.',
                        },
                        {
                          'url': require('../assets/img/stroller_alt.png'),
                          'titolo': 'Congue Gravida',
                          'bg': false,
                          'descrizione': 'Elipsis magna a terminal nulla elementum morbi elite forte maecenas est magno etos interdum vitae est.',
                        },
                        {
                          'url': require('../assets/img/globe_alt.png'),
                          'titolo': 'Maecenas Node',
                          'bg': true,
                          'descrizione': 'Praesent interdum est gravida vehicula est node maecenas loareet morbi a dpsos òictis mpvi, est praesent.a' ,
                        },
                        {
                          'url': require('../assets/img/bell_alt.png'),
                          'titolo': 'Praesent Morbi',
                          'bg': false,
                          'descrizione': 'Elipsis magna a terminal nulla elementum morbi elite forte maecenas est magno etos interdum vitae est.',
                        },

                      ]
      }
    }
}
</script>

<style lang="scss">
@import '../style/general.scss';

.bg-orange{
  background-color: $blaze_orange;
}

.bg-butterflu{
  background-color: $butterflu_bush;
}

#welcome{
  width: 1000px;
  margin: 0 auto;
  .row{
    display: flex;
    align-items: center;
    justify-content: space-between;
    
    .card{
      display: flex;
      justify-content: center;
      align-items: center;
      flex-direction: column;

      .wrapper-img{
        height: 200px;
        width: 200px;
        border-radius: 50%;
        display: flex;
        justify-content: center;
        align-items: center;        
      }
    }
  }
}

</style>