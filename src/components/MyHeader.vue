<template>
  <header>
    <!-- barra di navigazione -->
    <div class="wrapper-menu">
        <img class="logo" src="../assets/img/logo.png" alt="logo">
        <ul>
            <li v-for='(voci, indice) in vociMenu' 
                :key="indice" 
                :class="(voci.active?'active-menu':'')">
                    
                    <img :src="voci.url" :alt="voci.voce" :class="(voci.active?'img-position-bot':'img-position-top')">
                    <div class="menu-text">{{voci.voce}}</div>
            </li>
        </ul>
    </div>

    <!-- primo slider -->
    <div class="wrapper-jumbo-top">
        <div class="jumbo">
            <div class="wrapper-slider"
                @keyup.right="next" 
                @keyup.left="prev"      
                tabindex="0">
                
                <div class="slide">
                    <img :src="require ('../assets/img/team_01_0'+ counterSlideActive + '.jpg')" alt="slide">
                </div>
            </div>
            <div class="container-active">
                <div class="active-slider" 
                    v-for="(img, indice) in slideArray" :key="indice"
                    :class="(counterSlideActive == indice?'position-active': 'position-active-end')">
                </div>
            </div>
            
        </div>
    </div>

    <div class="wrapper-jumbo-bot">
        <div class="wrapper-menu">
            <h3>How to Enroll Your Child to a Class?</h3>
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
            counterSlideActive: 0,
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
                    ],
            slideArray: [
                            {
                                'active': true,
                            },
                            {
                                'active': false,
                            },
                            {
                                'active': false,
                            },
                        ],
        }
    },
    methods:{
        next(){
            if(this.counterSlideActive == this.slideArray.length - 1){
                this.counterSlideActive = 0;
            }else{
                this.counterSlideActive++;
            }
        },
        prev(){
            
            if(this.counterSlideActive == 0){
                this.counterSlideActive = this.slideArray.length - 1;
            }else{
                this.counterSlideActive--;
            }
        }
    }
}
</script>

<style lang="scss">
@import '../style/general.scss';
.flex-down{
    align-self: flex-end;
}
.position-active{
    align-self: flex-start;
}
.position-active-end{
    align-self: flex-end;
}

.active-menu{
    background-color: $blaze_orange;
    color: white;
}
.img-position-bot{
    object-position: bottom;
}
.img-position-top{
    object-position: top;
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
            height: 100px;
                li{
                    list-style: none;
                    display: flex;
                    flex-direction: column;
                    align-items: center;
                    justify-content: center;
                    padding: 0 15px;
                    &:hover{
                        background-color: $blaze_orange;
                        color: white;
                    }
                    &:hover > img{
                        object-position: bottom;
                    }
                    img{
                        height: 40px;
                        width: 40px;
                        object-fit: cover;
                        &:hover{
                            object-position: bottom;
                        }
                    }
                }
            }
        }
        .wrapper-jumbo-top{
            .jumbo{
                background-image: url('../assets/img/slider_slide1_background.png');
                height: 500px;
                position: relative;

                .wrapper-slider{
                    height: 80%;
                    display: flex;
                    align-items: center;
                    justify-content: center;
                    outline: none;
                    .slide{
                        height: 300px;
                        width: 300px;
                        padding: 0 20px;                        
                        img{
                            width: 100%;
                            border-radius: 50%;
                        }
                    }
                }
                .container-active{
                    position: absolute;
                    height: 30px;
                    bottom: 10%;
                    left: 50%;
                    transform: translate(-50%, -50%);
                    display: flex;
                    .active-slider{
                        height: 15px;
                        width: 50px;
                        border: 2px solid $blaze_orange;
                        margin-right: 10px;
                    }
                }
            }
        }
        .wrapper-jumbo-bot{
            background-image: url('../assets/img/pattern.png');
            height: 100px;
            color: white;
            button{
                background-color: $butterflu_bush;
                color: white;
                padding: 5px 10px;
                border: 2px solid white;
            }
        }
        
    }
</style>