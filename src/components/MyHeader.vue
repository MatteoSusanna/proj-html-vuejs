<template>
  <header>
    <div class="wrapper-menu">
        <img class="logo" src="../assets/img/logo.png" alt="logo">
        <ul>
            <li v-for='(voci, indice) in vociMenu' 
                :key="indice" 
                :class="(voci.active?'active-menu':'')">
                    <img :src="voci.url" :alt="voci.voce">
                    <div class="menu-text">{{voci.voce}}</div>
            </li>
        </ul>
    </div>

    <div class="wrapper-jumbo-top">
        <div class="jumbo">
            <img src="../assets/img/slider_slide1_background.png" alt="">
        </div>
    </div>

    <div class="wrapper-jumbo-bot">
        <div class="wrapper-menu">
            <h2>How to Enroll Your Child to a Class?</h2>
            <button>LEARN MORE > </button>
        </div>
    </div>
  </header>   
 
</template>

<script>
export default {
    nome: 'MyHeader',
    data(){
        return{
            vociMenu:[
                        {
                            'url': require ('../assets/img/home.png'),
                            'voce': 'Home',
                            'active': true
                        },
                        {
                            'url': require ('../assets/img/document.png'),
                            'voce': 'Pages',
                            'active': false
                        },
                        {
                            'url': require ('../assets/img/printer.png'),
                            'voce': 'Blog',
                            'active': false
                        },
                        {
                            'url': require ('../assets/img/cart.png'),
                            'voce': 'Shop',
                            'active': false
                        },
                        {
                            'url': require ('../assets/img/lab.png'),
                            'voce': 'Shortcodes',
                            'active': false
                        },
                        {
                            'url': require ('../assets/img/chat.png'),
                            'voce': 'Support',
                            'active': false
                        },
                        {
                            'url': require ('../assets/img/envelope.png'),
                            'voce': 'Contact',
                            'active': false
                        },
                    ]
        }
    }
}
</script>

<style lang="scss">
@import '../style/general.scss';

.active-menu{
    background-color: $blaze_orange;
    color: white;
}
    header{
        .wrapper-menu{
            height: 100px;
            display: flex;
            align-items: center;
            justify-content: space-between;
            width: 1000px;
            margin: 0 auto;
            .logo{
            height: 100%;
            }
            ul{
            display: flex;
            justify-content: space-between;
            width: 500px;
            height: 70px;
                li{
                    list-style: none;
                    display: flex;
                    flex-direction: column;
                    align-items: center;
                    justify-content: center;
                    img{
                        height: 40px;
                        width: 40px;
                        object-fit: cover;
                        object-position: top;
                        &:hover{
                            object-position: bottom;
                        }
                    }
                }
            }
        }
        .wrapper-jumbo-top{
            
            .jumbo{
                height: 500px;
                img{
                width: 100%;
                height: 100%;
                object-fit: fill;
                }
            }
            
        }
        .wrapper-jumbo-bot{
            height: 100px;
            background-color: $butterflu_bush;
        }
        
    }
</style>