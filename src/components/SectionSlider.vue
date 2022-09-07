<template>
    <section id="slider">
        <div class="row">
            <div class="col" v-for="(colonna, indice) in colsArray" :key="indice">
                <div class="number">{{colonna.numero}}</div>
                <h3 class="ptb">{{colonna.titolo}}</h3>
                <span>{{colonna.descrizione}}</span>
            </div>
        </div>
    </section>
</template>

<script>
export default {
    nome: 'SectionSlider',
    data(){
        return{
            colsArray:  [
                            {
                                numero: '507',
                                titolo: 'Our Pupils',
                                descrizione: 'Pulvinar forte maestro node terminal est elipsis prism.'
                            },
                            {
                                numero: '235',
                                titolo: 'Teaching Hours',
                                descrizione: 'Elipsis morbi nulla a metro interdum vitae elite.'
                            },
                            {
                                numero: '100%',
                                titolo: 'Satisfied Parents',
                                descrizione: 'Elementum pulvinar detos diaspis movum blandit'
                            },
                            {
                                numero: '1050',
                                titolo: 'Our Pupils',
                                descrizione: 'Pulvinar forte maestro node terminal est elipsis prism.'
                            },
                        ]
        }
    }
}
</script>

<style lang="scss">
@import '../style/general.scss';

#slider{
    background-image: url('../assets/img/parallax_01.jpg');
    background-position: center; 
    color: white;
    height: 500px;
    .wrapper-img{
        height: 500px;
        img{
            width: 100%;
            height: 100%;
            object-fit: cover;
        }
    }
    .row{
        width: 1000px;
        height: 100%;
        margin: 0 auto;
        display: flex;
        justify-content: space-between;
        align-items: center;
        .col{
            width: calc(100% / 4 - 0.5rem);
            text-align: center;
            .number{
                height: 200px;
                width: 200px;
                margin: 0 auto;
                border: 2px solid white;
                font-size: 50px;
                border-radius: 50%;
                text-align: center;
                line-height: 200px;
                &:hover{
                    background-color: $blaze_orange;
                }
            }
        }
    }
}

</style>