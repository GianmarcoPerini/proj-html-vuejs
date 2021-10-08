<template>
    <div class="card">
        <i class="fs-1" :class="icon"></i>
        <h4 class="mb-3 mt-5">{{title}}</h4>
        <p>{{text}}</p>
    </div>
</template>

<script>
export default {
    name: 'Cards',
    props: {
        title: String,
        text: String,
        icon: String,
    }

}
</script>

<style lang="scss" scoped>
@import '../variables/color';


    .card{
        width: 100%;
        padding: 30px;
        margin: 15px 10px;
        border: none;
        border-radius: 20px;
        box-shadow: $shadowLightBlack;
        overflow: hidden;
        position: relative;
        background-color: white;
        z-index: 1;
        

        &::before {
            position: absolute;
            content: "";
            top: 0;
            right: 0;
            bottom: 0;
            left: 0;
            background-image: linear-gradient( 45deg, #05d9a5, #aee77f );
            z-index: -1;
            transition: opacity 200ms linear;
            opacity: 0;
        }

        &:hover::before {
            opacity: 1;
        }

        &:hover p,
        &:hover{
            color: white;
        }

        p{
            font-family: dosis;
            color: $textPrimary;
        }
}










</style>