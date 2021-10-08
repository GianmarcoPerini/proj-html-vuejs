<template>
    <div class="sponsor">
        <img :src=" require('../../assets/' + path + '.png')  " alt="">
    </div>
</template>

<script>
export default {
    name: 'Sponsor',
    props: {
        path: String,
    }

}
</script>

<style lang="scss" scoped>
@import '../variables/color';

.sponsor{
    margin-top: 100px;
}

</style>