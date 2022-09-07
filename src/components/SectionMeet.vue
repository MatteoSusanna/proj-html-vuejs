<template>
    <section id="meet">
        <div class="text-center">
            <h2 class="pt">Meet Our Staff</h2>
            <p class="ptb">Our preschool program has four dedicated classes</p>
            <img class="pb" src="../assets/img/header_divider.png" alt="divisore">
        </div>

        <div class="row">
            <h2 class="col">We provided four classes with nine to twernty children each aged twelve month to five years of age.</h2>
            <p class="col">Prasent arcu gravida vehicula est node maecenas loareet morbi a dosis lactus. Urna aget lacinia eleifend praesent luctus a arcu quis facilisis venenatis. Aenean interdum, nibh vitae sodales, magna ante feugiat elit maecenas.</p>
        </div>
        

        <div class="wrapper-card">
            <div class="card" v-for="(dati, indice) in meetArray" :key="indice">

                <div class="left">
                    <div class="img">
                        <img :src="dati.img" :alt="dati.nome">
                        <div class="overPlus d-none">
                            <i class="fa-solid fa-plus"></i>
                        </div>
                    </div>
                    

                    <div class="testo">
                        <h4>{{dati.nome}}</h4>
                        <span>{{dati.ruolo}}</span>
                    </div>
                </div>

                <div class="right">
                    <div class="vingolette"><img src="../assets/img/quote.png" alt="virgolette"></div>
                    
                    <div></div>
                    <p>{{dati.descrizione}}</p>
                    <div class="wrapper-social">
                        <div class="social">
                            <img :src="dati.social1" alt="social">
                        </div>
                        <div class="social">
                            <img :src="dati.social2" alt="social">
                        </div>
                        <div class="social">
                            <img :src="dati.social3" alt="social">
                        </div>
                    </div>
                </div>
            </div>
        </div>

    </section>
</template>

<script>
export default {
    nome: 'SectionMeet',
    data(){
        return{
            meetArray:  [
                            {
                                img: require('../assets/img/team_04.jpg'),
                                nome: 'Ruth Richie',
                                ruolo: 'Teacher',
                                descrizione: 'I have just finished my studies in Early Childhood Education, and i am also the kids yoga teacher here at Fable. I enjoy cooking, swimming and bike riding in my free time.',
                                social1: require('../assets/img/mail.png'),
                                social2: require('../assets/img/facebook.png'),
                                social3: require('../assets/img/pinterest.png'),
                            },
                            {
                                img: require('../assets/img/team_03.jpg'),
                                nome: 'Katie Willmore',
                                ruolo: 'Assistant Teacher',
                                descrizione: 'My name is Katie. I grew up and studied in Canada. this is my second year at Fabie and love every minute of it, making the childrens learning experience fun.',
                                social1: require('../assets/img/dribbble.png'),
                                social2: require('../assets/img/stumbleupon.png'),
                                social3: require('../assets/img/instagram.png'),
                            },
                            {
                                img: require('../assets/img/team_02.jpg'),
                                nome: 'Angelica Watson',
                                ruolo: 'Lead Teacher',
                                descrizione: 'I hold a dagree in Early Childhood Education and an advanced English lenguage cerificate. I have been working as a kindergarten teacher since 2002.',
                                social1: require('../assets/img/bing.png'),
                                social2: require('../assets/img/twitter.png'),
                                social3: require('../assets/img/linkedin.png'),
                            },
                            {
                                img: require('../assets/img/team_01.jpg'),
                                nome: 'Angela Lynn',
                                ruolo: 'Teacher',
                                descrizione: 'I have just finished my studies in Early Childhood Education, and i am also the kids yoga teacher here at Fable. I enjoy cooking, swimming and bike riding in my free time.',
                                social1: require('../assets/img/stumbleupon.png'),
                                social2: require('../assets/img/bing.png'),
                                social3: require('../assets/img/dribbble.png'),
                            },
                        ]
        }
    }
}
</script>

<style lang="scss">
@import '../style/general.scss';

#meet{
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

    .wrapper-card{
        display: flex;
        flex-wrap: wrap;
        margin-top: 50px;
        .card{
        display: flex;
        width: calc(100% / 2);
        margin-bottom: 30px;
        position: relative;
        .left{
            width: 50%;
            position: relative;
            .img{
                img{
                    width: 100%;
                    object-fit: cover;
                    &:hover ~ .overPlus{
                        display: block;
                    }  
                }
            }
            .testo{
                text-align: center;
                margin: 20px 0;
            }
            .overPlus{
                position: absolute;
                bottom: 50%;
                left: 50%;
                transform: translate(-50%);
                height: 80px;
                width: 80px;
                border-radius: 50%;
                background-color: $butterflu_bush;
                opacity: 0.5;
                text-align: center;
                line-height: 80px;
                &:hover{
                        display: block;
                    }
                i{
                    color: white;
                }

            }
        }
        .right{
            width: 50%;
            padding: 15px;
            display: flex;
            flex-direction: column;
            justify-content: space-between;
            .vingolette{
                border: 1px solid $blaze_orange;
                width: 90px;
                height: 40px;
                text-align: right;
                padding: 0 10px;
                position: absolute;
                right: calc(50% - 70px);
            }
            .wrapper-social{
                display: flex;
                .social{
                    width: 50px;
                    height: 50px;
                    background-color: $blaze_orange;
                    display: flex;
                    align-items: center;
                    justify-content: center;
                    margin-right: 5px;
                    &:hover{
                        transform: scale(1.1);
                        border: 2px solid $butterflu_bush;
                    }
                }   
            }
           
        }
    }

    }
    
}
</style>