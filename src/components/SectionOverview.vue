<template>
  <section id="overview">
    <div class="container">
        <div class="col">
            <div class="button">
                <button>Overview</button>
                <button>Our Mission</button>
            </div>
            <div class="overview-wrapper">
                <h2>Our philosophy is learning through play as we offer a stimulation environment for children.</h2>
                
                <div class="row" v-for="(over, indice) in  overviewArray" :key="indice">
                    <div class="img-wrap">
                        <img :src="over.url" :alt="over.titolo">
                    </div>
                    <div class="testo">
                        <h4>{{over.titolo}}</h4>
                        <p>{{over.descrizione}}</p>
                    </div>
                </div>
            </div>
        </div>

        <div class="col">
            <div class="wrapper-slider1">
                <div class="img-active">
                    <img src="" alt="">
                </div>
                <div class="list-img">

                </div>
            </div>
        </div>
    </div>
  </section>
</template>

<script>
export default {
    nome: 'SectionOverview',
    data(){
        return{
            overviewArray:  [
                                {
                                    'url': require('../assets/img/clock_alt.png'),
                                    'titolo': 'Full Day Sessions',
                                    'descrizione': 'Pulvinar est metro ligula bladt maecenas retrum gravida cuprum. Maecenas node estibulum.',
                                },
                                {
                                    'url': require('../assets/img/diagram_alt.png'),
                                    'titolo': 'VariedClasses',
                                    'descrizione': 'Pulvinar est metro ligula bladt maecenas retrum gravida cuprum. Maecenas node estibulum.',
                                }
                            ]
        }
    }
}
</script>

<style lang="scss">
@import '../style/general.scss';

h2, h4{
    color: $butterflu_bush;
}

#overview{
    background-color: $bon_jour;
    padding: 40px 0;
    .container{
        display: flex;
        justify-content: space-between;
        align-items: center;
        width: 1000px;
        margin: 0 auto;

        .col{
            width: 50%;

            .button{
                button{
                    background-color: $blaze_orange;
                    border: none;
                    color: white;
                    padding: 10px 15px;
                    margin-right: 10px;
                    margin-bottom: 10px;
                }
            }
            .overview-wrapper{

                .row{
                    display: flex;
                    justify-content: space-between;
                    align-items: center;
                    margin: 20px 0;
                    .img-wrap{
                        height: 70px;
                        width: 110px;
                        display: flex;
                        align-items: center;
                        justify-content: center;
                        border-radius: 50%;
                        background-color: $blaze_orange;
                    }
                    .testo{
                        margin-left: 20px;
                        h4{
                            margin-bottom: 10px;
                        }
                    }
                }

            }
        }
        .wrapper-slider1{
            display: flex;
            flex-direction: column;
            .img-active{
                height: 80%;
                img{
                    width: 100%;
                }
            }
            .list-img{
                height: 20%;
                img{
                    width: 20%
                }
            }
        }
    }
}

</style>