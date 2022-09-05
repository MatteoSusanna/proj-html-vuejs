<template>
    <section id="slider">
        <div class="row">
            <div class="col">
                <div class="number"></div>
                <h3></h3>
                <p></p>
            </div>
        </div>
    </section>
</template>

<script>
export default {
    nome: 'SectionSlider',
    data(){
        return{
            colsArray: []
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
    padding: 20px;
    height: 500px;
}

</style>