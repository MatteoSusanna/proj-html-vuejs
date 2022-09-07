<template>
    <section id="what">
        <div class="text-center">
            <h2 class="pt">What's New</h2>
            <p class="ptb">Keep up to date with the latest news</p>
            <img src="../assets/img/header_divider.png" alt="divisore">
        </div>

        <div class="row">
            <div class="col" v-for="(attivita, indice) in whatArray" :key="indice">
                <p>{{attivita.data}}</p>
                <div class="wrap-img">
                    <img :src="attivita.url" alt="attività bambini">
                    <div class="numero">{{attivita.numero}}</div>
                </div>
                <h2 class="ptb">{{attivita.titolo}}</h2>
                <p>{{attivita.descrizione}}</p>
                <div class="separatore"></div>
                <div class="container-attivita">
                    <img class="mr-10" :src="attivita.url1" alt="nome insegnante">
                    <p class="mr-20">{{attivita.nome}}</p>
                    <img class="mr-10" :src="attivita.url2" alt="tipo attività">
                    <p>{{attivita.attivita}}</p>
                </div>
            </div>
        </div>
        <div class="text-center">
            <button>GO TO BLOG <i class="fa-solid fa-angle-right"></i></button>
        </div>
    </section>
</template>

<script>
export default {
    nome: 'SectionWhat',
    data(){
        return{
            whatArray:  [
                            {
                                data: 'October 03, 2014',
                                url: require('../assets/img/blog_09-300x180.jpg'),
                                numero: '42',
                                titolo: 'Drowing and Painting',
                                descrizione: 'Magna est consectetur interdum modest dictum. Curabitur est faucibus malesuada esttincidunt etos et mauris, nunc at libero govum est cuprum [...]',
                                url1: require('../assets/img/author.png'),
                                nome: 'Anna Brown',
                                url2: require('../assets/img/category.png'),
                                attivita: 'Events, Fun',

                            },
                            {
                                data: 'October 03, 2014',
                                url: require('../assets/img/blog_10-300x180.jpg'),
                                numero: '19',
                                titolo: 'Fall Parents Meeting Day',
                                descrizione: 'Magna est consectetur interdum modest dictum. Curabitur est faucibus malesuada esttincidunt etos et mauris, nunc at libero govum est cuprum [...]',
                                url1: require('../assets/img/author.png'),
                                nome: 'Anna Brown',
                                url2: require('../assets/img/category.png'),
                                attivita: 'Dance, Education',

                            },
                            {
                                data: 'September 20,2014',
                                url: require('../assets/img/blog_08-300x180.jpg'),
                                numero: '22',
                                titolo: 'Birthday in Kindergarten',
                                descrizione: 'Magna est consectetur interdum modest dictum. Curabitur est faucibus malesuada esttincidunt etos et mauris, nunc at libero govum est cuprum [...]',
                                url1: require('../assets/img/author.png'),
                                nome: 'Anna Brown',
                                url2: require('../assets/img/category.png'),
                                attivita: 'Games, General',

                            },
                        ]
        }
    }
}
</script>

<style scoped lang="scss">
@import '../style/general.scss';
button{
    border: none;
    background-color: $blaze_orange;
    color: white;
    padding: 10px;
    margin-top: 30px;
}

#what{
    width: 1000px;
    margin: 0 auto;
    padding-bottom: 40px;
    .row{
        display: flex;
        justify-content: space-between;
        margin-top: 50px;
        .col{
            width: calc(100% / 3 - 1.5rem);
            .wrap-img{
                position: relative;
                height: 200px;
                img{
                    width: 100%;
                    height: 100%;
                }
                .numero{
                    position: absolute;
                    bottom: 0;
                    right: 0;
                    color: white;
                    background-color: $blaze_orange;
                    height: 40px;
                    width: 40px;
                    text-align: center;
                    line-height: 40px;
                }
            }

            .container-attivita{
                margin-top: 30px;
                display: flex;
                border-top: 1px solid $bon_jour;
                padding-top: 10px;
            }
            
        }
    }

}

</style>