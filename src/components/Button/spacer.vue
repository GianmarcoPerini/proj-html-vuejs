<template>
    <div class="spacer d-flex mt-4 mb-4">
        <div class="spacer-one h-100 w-25 bg-primary me-1"></div>
        <div class="spacer-two h-100 w-75 bg-primary"></div>
    </div> 
</template>

<script>
export default {
    name: 'Spacer'

}
</script>

<style lang="scss" scoped>
@import '../variables/color';

    .spacer{
        width: 50px;
        height: 5px;
        
        .spacer-one,
        .spacer-two{
            border-radius: 10px;
            background-image: linear-gradient(45deg, rgba(151,225,95,1) 0%, rgba(1,217,165,1) 100%);
        }
    }

</style>