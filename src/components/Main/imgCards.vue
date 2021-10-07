<template>
    <div class="imgCard">
        <img :src="require('../../assets/' + path + '.jpg')" alt="">
    </div>
</template>

<script>
export default {
    name: 'imgCard',
    props: {
        path: String,
    }

}
</script>

<style lang="scss">

.imgCard{
    border-radius: 4px;
    overflow: hidden;

    img{
        width: 100%;
    }
}


</style>