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
        width: calc(100% / 2 - 20px);
        padding: 30px;
        margin: 15px 10px;
        border: none;
        border-radius: 20px;
        box-shadow: 7px 7px 12px rgba(0,0,0,.1);
        position: relative;


        &:hover{
            background-image: $gradientGreen;
            opacity: 1;
        }

        p{
            font-family: roboto;
            color: $textPrimary;
            font-size: .8rem;
        }
}




</style>