<template>
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

    button{
        background-image: linear-gradient(45deg, rgba(151,225,95,1) 0%, rgba(1,217,165,1) 100%);
        border: none;
        border-radius: 30px;
        padding: 15px 45px;
        transition: background-image 300ms linear;
        font-size: .8rem;
        box-shadow: 10px 5px 20px 5px rgba(1,217,165, .3);

        &:hover{
            background-image: linear-gradient(45deg, rgba(61,61,61,1) 0%, rgba(0,0,0,1) 100%);
            box-shadow: 10px 5px 20px 5px rgba(61,61,61,.3);
        }
    }

</style>