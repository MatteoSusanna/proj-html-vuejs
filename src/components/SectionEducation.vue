<template>
    <section id="education">
        <div class="row">
            <div class="col-list">
                <h2>We have been educating children for over fifteen years. Our goal is to create a place that engages eash child.</h2>
                <p class="ptb">Praesent arcu gravida vahicula est node maecenas loareet morbi a dosis luctus. Urna aget lacinia eleifend praesent luctus a arcu quis facilisis venenatis aenen interdum.</p>
                
                <ul>
                    <li v-for="(lista,indice) in listArray" :key="indice">
                        <i class="fa-regular fa-square-check"></i>
                        <span>{{lista.testo}}</span>
                    </li>
                </ul>
            </div>
            <div class="col-card">
                <div class="card" v-for="(lista,indice) in learninArray" :key="indice">
                    <div class="wrap-image">
                        <img :src="lista.url">
                    </div>
                    <h2 class="ptb">{{lista.titolo}}</h2>
                    <p>{{lista.testo}}</p>
                </div>
            </div>
        </div>
    </section>
</template>

<script>
export default {
    nome: 'SectionEducation',
    data(){
        return{
            listArray:  [
                            {
                                testo: 'Comprehensive reporting on individual achievement'
                            },
                            {
                                testo: 'Educational field trips and school presentations'
                            },
                            {
                                testo: 'individual attention in a small-class setting'
                            },
                            {
                                testo: 'Learning program with after-school care'
                            },
                            {
                                testo: 'Opportunities to carry out scientific investigations'
                            },
                            {
                                testo: 'Positive learning environment for your child'
                            },
                        ],
            learninArray:   [
                                {
                                    url: require('../assets/img/toy.png'),
                                    titolo: 'Learning & Fun',
                                    testo: 'Praesent modea est gravida node vehicula luctus.'
                                },
                                {
                                    url: require('../assets/img/meal.png'),
                                    titolo: 'Healthy Meals',
                                    testo: 'Terminal interdum a eleifend maecenas est morbi.'
                                },
                                {
                                    url: require('../assets/img/school.png'),
                                    titolo: 'Friendly Place',
                                    testo: 'Terminal interdum a eleifend maecenas est morbi.'
                                },
                                {
                                    url: require('../assets/img/shield.png'),
                                    titolo: 'Children Safety',
                                    testo: 'Praesent modea est gravida node vehicula luctus.'
                                },
                            ]
        
        }
    }
}
</script>

<style lang="scss">
@import '../style/general.scss';
p{
    color: gray;
}

#education{
    background-color: $bon_jour;
    padding: 30px;
    .row{
        width: 1000px;
        margin: 0 auto;
        display: flex;
        justify-content: space-between;
        .col-list{
            width: 50%;
            ul{
                li{
                    list-style: none;
                    margin: 5px 0;
                    color: grey;
                    i{
                        color: $blaze_orange;
                        margin-right: 5px;
                        font-size: 25px;
                    }
                }
            }
        }
        .col-card{
            width: 50%;
            display: flex;
            flex-wrap: wrap;
            .card{
                width: calc(100% / 2 - 1rem);
                text-align: center;

                .wrap-image{
                    height: 70px;
                    width: 70px;
                    border-radius: 50%;
                    background-color: white;
                    margin: 0 auto;
                    display: flex;
                    align-items: center;
                    justify-content: center;
                }
            }
        }
    }
}

</style>