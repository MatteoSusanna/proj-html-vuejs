<template>
   <section id="contact">
        <div class="text-center">
            <h2 class="pt">Contact Us</h2>
            <p class="ptb">Our postal address and contact details</p>
            <img src="../assets/img/header_divider.png" alt="divisore">
        </div>

        <div class="row">
            <div class="col" v-for="(contatti, indice) in contactArray" :key="indice">
                <img :src="contatti.url" alt="contatto">
                <h2 class="ptb">{{contatti.titolo}}</h2>
                <p>{{contatti.dato1}}</p>
                <p class="ptb-5">{{contatti.dato2}}</p>
                <p>{{contatti.dato3}}</p>
            </div>
        </div>

        <MyForm />

   </section>
</template>

<script>
import MyForm from './MyForm'

export default {
    nome: 'SectionContact',
    components:{
        MyForm,
    },
    data(){
        return{
            contactArray:   [
                                {
                                    url: require('../assets/img/envelope(1).png'),
                                    titolo: 'Postal Address',
                                    dato1: 'Fable Care Center',
                                    dato2: '85 Fentiman Ave',
                                    dato3: 'Ottawa, ON K1S 0T7',
                                },
                                {
                                    url: require('../assets/img/mobile.png'),
                                    titolo: 'Phone & E-mail',
                                    dato1: 'Phone: 1-800-64-38',
                                    dato2: 'Fax: 1-800-64-39',
                                    dato3: 'Office@fable.com',
                                },
                                {
                                    url: require('../assets/img/clock.png'),
                                    titolo: 'Business Hours',
                                    dato1: 'Monday- Friday',
                                    dato2: '8.00 am - 5.00 pm',
                                    dato3: 'Weekend Closed',
                                },
                                {
                                    url: require('../assets/img/document(1).png'),
                                    titolo: 'Sessions',
                                    dato1: 'Mornings, 8 am - 12 noon',
                                    dato2: 'Afternoons, 1 pm - 5 pm',
                                    dato3: 'Full Day, 8 am - 5pm',
                                },
                            ]
        }
    }
}
</script>

<style lang="scss">
@import '../style/general.scss';

#contact{
    width: 1000px;
    margin: 0 auto;
    .row{
        display: flex;
        justify-content: space-between;
        margin-top: 50px;
        .col{
            width: calc(100% / 4 - 1rem);
            text-align: center;
            &:hover{
                transform: scale(1.2);
            }
        }
    }
}
</style>