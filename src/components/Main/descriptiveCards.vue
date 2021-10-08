<template>
<div class="position-relative">
    <div class="box">
        <img class="w-100" :src="require('../../assets/' + path + '.jpg') " alt="">
    </div>
    <div class="description position-absolute">
            <p class="date mb-1">{{date}} {{creator}}</p>
            <i class="me-1 d-inline-block fas fa-circle"></i>
            <p class="d-inline-block title">{{text}}</p>
            
        </div>
</div>

</template>

<script>
export default {
    name: 'desciptiveCards',
    props: {
        date: String,
        path: String,
        text: String,
        creator: String,
    }

}
</script>

<style lang="scss" scoped>
@import '../variables/color';

.box{
    background-color: red;
    width: 100%;
}

.description{
    background-color: white;
    border-radius: 10px;
    width: 80%;
    bottom: -20px;
    left: 50%;
    transform: translateX(-50%);
    padding: 15px 0 0 15px;

    p{
        font-family: work sans;
    }

    i{
        font-size: 6px;
        vertical-align: middle;
        color: $textActive;
    }

    .date{
        font-size: .6rem;
        color: $textPrimary;
    }

    .title{
        font-size: .9rem;
    }
}
</style>