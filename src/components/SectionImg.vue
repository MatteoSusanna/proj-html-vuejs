<template>
    <section id="image">
        <div class="contenitore-img" >
            <div class="img"  v-for="(image, indice) in imgArray" :key="indice">
                <img :src="image.url" alt="bambino">
            </div>
        </div>
        <div class="wrapper-jumbo-bot">
        <div class="wrapper-menu">
            <h3>How to Enroll Your Child to a Class?</h3>
            <button>LEARN MORE > </button>
        </div>
    </div>
    </section>
</template>

<script>
export default {
    nome: 'SectionImg',
    data(){
        return{
            imgArray:   [
                            {
                                url: require('../assets/img/gallery_01-690x506.jpg')
                            },
                            {
                                url: require('../assets/img/gallery_02-690x506.jpg')
                            },
                            {
                                url: require('../assets/img/gallery_03-690x506.jpg')
                            },
                            {
                                url: require('../assets/img/gallery_04-690x506.jpg')
                            },
                        ]
        }
    },
}
</script>

<style lang="scss">
@import '../style/general.scss';

#image{
    .contenitore-img{
        display: flex;
        .img{
            width: calc(100% / 4);
            img{
                width: 100%;
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