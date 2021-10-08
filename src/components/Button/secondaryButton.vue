<template>
    <!-- Bottone che in base alla prop passata dal padre cambia il testo dinamicamente -->
    <button class="text-white"> {{btnElement}} </button>
</template>

<script>
export default {
    name: 'secondaryButton',
    props: {
        btnElement: String
    }
    

}
</script>

<style lang="scss" scoped>
@import '../variables/color';
    button{
        background-image: $gradientBlack;
        box-shadow: $shadowBlack;
        border: none;
        border-radius: 30px;
        padding: 15px 45px;
        font-size: .8rem;
        position: relative;
        z-index: 1;
        overflow: hidden;
        transition: box-shadow 200ms;

        &::before{
            position: absolute;
            content: "";
            inset: 0 0 0 0;
            background-image: $gradientGreen;
            z-index: -1;
            transition: opacity 200ms linear;
            opacity: 0;
        }

        &:hover::before{
            opacity: 1;
        }

        &:hover{
            box-shadow: $shadowGreen;
        }
    }

</style>