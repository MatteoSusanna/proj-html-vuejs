<template>
  <section id="slider2">
        <div class="row">
            <div class="col" v-for="(colonna, indice) in slider2Array" :key="indice">
                <div class="number"><img :src="colonna.url" alt="virgolette"></div>
                <h3 class="ptb">{{colonna.titolo}}</h3>
                <div class="d-flex pb">
                    <span class="separatore"></span>
                </div>
                <span>{{colonna.autore}}</span>
            </div>
        </div>
    </section>
</template>

<script>
export default {
    nome: 'SectionSlider2',
    data(){
        return{
            slider2Array:   [
                                {
                                    url: require('../assets/img/quote_alt.png'),
                                    titolo: 'Fable Kindergarten is a great place for my daughter to start her schooling experience. its welcoming and safe and my daughter loves being there.',
                                    autore: 'Joe R.Hamblen',
                                }
                            ]
        }
    },
}
</script>

<style lang="scss">
#slider2{
    background-image: url('../assets/img/parallax_01.jpg');
    background-position: center; 
    color: white;
    padding: 20px;
    height: 500px;
    .row{
        width: 1000px;
        height: 100%;
        margin: 0 auto;
        display: flex;
        justify-content: space-between;
        align-items: center;
        .col{
            text-align: center;
            h3{
                font-weight: 500;
                font-size: 40px;
            }
            .separatore{
                background-color: white;
                height: 1px;
                width: 60px;
            }
            .number{
                height: 100px;
                width: 100px;
                margin: 0 auto;
                border: 2px solid white;
                font-size: 50px;
                border-radius: 50%;
                text-align: center;
                line-height: 100px;
            }
        }
    }
}

</style>
