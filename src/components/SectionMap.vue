<template>
    <section id="map">
        <iframe src="https://www.google.com/maps/embed?pb=!1m18!1m12!1m3!1d2801.6612510426353!2d-75.6787496493225!3d45.39600374591053!2m3!1f0!2f0!3f0!3m2!1i1024!2i768!4f13.1!3m3!1m2!1s0x0%3A0xef374fb5a3427474!2zNDXCsDIzJzQ1LjYiTiA3NcKwNDAnMzUuNiJX!5e0!3m2!1sit!2sit!4v1662468427508!5m2!1sit!2sit" 
            width="100%" 
            height="100%" 
            style="border: none;" 
            allowfullscreen="" 
            loading="lazy" 
            referrerpolicy="no-referrer-when-downgrade">
        </iframe>
    </section>
</template>

<script>
export default {
    nome: 'SectionMap'
}
</script>

<style lang="scss">
@import '../style/general.scss';

#map{
    height: 400px;
    background-color: $bon_jour;
}

</style>