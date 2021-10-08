<template>
    <!-- Bottone che in base alla prop passata dal padre cambia il testo dinamicamente -->
    <button class="text-white"> {{btnElement}} </button>
</template>

<script>
export default {
    name: 'primaryButton',
    props: {
        btnElement: String
    }
}
</script>

<style lang="scss" scoped>
@import '../variables/color';

    button{
        background-image: $gradientGreen;
        border: none;
        border-radius: 30px;
        padding: 15px 45px;
        transition: background-image 300ms linear;
        font-size: .8rem;
        box-shadow: $shadowGreen;
        position: relative;
        overflow: hidden;
        z-index: 1;
        transition: box-shadow 200ms;

        &::before{
            position: absolute;
            content: "";
            inset: 0 0 0 0;
            background-image: $gradientBlack;
            z-index: -1;
            transition: opacity 200ms linear;
            opacity: 0;
        }

        &:hover::before{
            opacity: 1;
        }

        &:hover{
            box-shadow: $shadowBlack;
        }


    }

</style>