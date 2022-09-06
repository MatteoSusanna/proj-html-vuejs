<template>
    <form>
        <div class="container-form">
            <div class="col-left col">
                <input type="text" placeholder="Your Name *" required>
                <input type="text" placeholder="Your E-mail *" required>
                <input type="text" placeholder="Subject">
            </div>
            <div class="col-right col">
                <textarea cols="50" rows="10" placeholder="Your Message *" required></textarea>
            </div>
        </div>
        <div class="text-center">
            <button>SEND MESSAGE</button>
        </div>
    </form>
</template>

<script>
export default {
    nome: 'MyForm'
}
</script>

<style scoped lang="scss">
@import '../style/general.scss';
.col{
    width: 50%;
}

button{
    border: none;
    background-color: $blaze_orange;
    color: white;
    padding: 10px;
}

form{
    margin-bottom: 40px;
}

 .container-form{
    display: flex;
    justify-content: space-between;
    height: 150px;
    margin: 50px 0;
    .col-right{
        textarea{
            width: calc(100% - 1rem);
            height: 100%;
            padding: 10px;
            border-color: $bon_jour;
        }
    }
    .col-left{
        display: flex;
        flex-direction: column;
        justify-content: space-between;
        input{
            width: calc(100% - 1rem);
            height: 25%;
            padding: 10px;
            border: 1px solid $bon_jour;
        }
    }
 }


</style>
