<template>
    <section id="ourClasses">
        <div class="text-center">
            <h2 class="pt">Our Classes</h2>
            <p class="ptb">Our preschool program has four dedicated classes</p>
            <img src="../assets/img/header_divider.png" alt="divisore">
        </div>

        <div class="row">
            <h2 class="col">We provided four classes with nine to twernty children each aged twelve month to five years of age.</h2>
            <p class="col">Prasent arcu gravida vehicula est node maecenas loareet morbi a dosis lactus. Urna aget lacinia eleifend praesent luctus a arcu quis facilisis venenatis. Aenean interdum, nibh vitae sodales, magna ante feugiat elit maecenas.</p>
        </div>

        <div class="card-class">
            <div class="card-bim" v-for="(classe, indice) in classArray" :key="indice">
                <div class="text">
                    <div class="classe">
                        <h3>{{classe.classe}}</h3>
                        <span>Class name</span>
                    </div>
                    <div class="eta">
                        <div>
                            <h3>{{classe.anni}}</h3>
                            <span>Month olds</span>
                        </div>
                        <span class="divisore"></span>
                        <div>
                            <h3>{{classe.size}}</h3>
                            <span>CLass size</span>
                        </div>
                    </div>
                </div>
                <div class="bambino">
                    <img :src="classe.url" alt="bambino">
                    <div class="read">Read More > </div>
                </div>
            </div>
        </div>
    </section>
</template>

<script>
export default {
    nome: 'SectionClasse',
    data(){
        return{
            classArray: [
                            {
                                url: require('../assets/img/class_01-690x506.jpg'),
                                classe: 'Little Lambs',
                                anni: '12-24',
                                size: '9'
                            },
                            {
                                url: require('../assets/img/class_02-690x506.jpg'),
                                classe: 'Bouncy Bears',
                                anni: '2-3',
                                size: '12'
                            },
                            {
                                url: require('../assets/img/class_03-690x506.jpg'),
                                classe: 'Tenderhearts',
                                anni: '3-4',
                                size: '15'
                            },
                            {
                                url: require('../assets/img/class_04-690x506.jpg'),
                                classe: 'Shining Stars',
                                anni: '4-5',
                                size: '20'
                            },
                        ]
        }
    }
}
</script>

<style lang="scss">
@import '../style/general.scss';

#ourClasses{
    width: 1000px;
    margin: 0 auto;
    .row{
        display: flex;
        justify-content: space-between;
        .col{
            width: 45%;
            font-weight: 500;
        }
    }

    .card-class{
        display: flex;
        justify-content: space-between;
        flex-wrap: wrap;
        margin: 50px 0;
        color: white;
        .card-bim{
            display: flex;
            justify-content: space-between;
            width: calc(100% / 2 - 1rem);
            background-color: $butterflu_bush;            
            height: 170px;
            margin-bottom: 2rem;
            .text{
                display: flex;
                flex-direction: column;
                justify-content: space-between;
                padding: 15px;
                .eta{
                    display: flex;
                    .divisore{
                        background-color: white;
                        display: inline-block;
                        width: 1px;
                        height: 40px;
                        margin: 0 10px;
                    }
                }
            }
            .bambino{
                height: 170px;
                position: relative;
                img{
                    width: 100%;
                    height: 100%;
                }
                .read{
                    position: absolute;
                    color: white;
                    width: 100px;
                    background-color: $blaze_orange;
                    padding: 7px 0px;
                    padding-left: 5px;
                    bottom: 0;
                    left: calc(100% - 100px);
                }
            }
        }
    }

}

</style>