<template>
    <div class="button d-flex align-items-center">
        <div class="single-button" @click="goTo(i)" v-for="(el, i) in btnElements" :key="i"  :class="(i == indexCount) ? 'active' : '' "> {{el}} </div>
    </div>
</template>

<script>
export default {
    name:'multiButton',
    props: {
        btnElements: Array
    },
    data(){
        return{
            button: this.elementi,
            indexCount: 1,
        }
    },

    methods:{
        goTo(index){
            this.indexCount = index
            console.log(index);
        }
    }

}
</script>

<style lang="scss" scoped>
@import '../variables/color';

.button{
    background-image: linear-gradient(45deg, rgb(90, 90, 90) 0%, $bgSecondary 100%);
    border-radius: 25px;
}
.single-button{
    padding: 9px 15px;
    border-radius: 20px;
    margin: 4px;
    color: $textLight;
    cursor: pointer;
}

.active{
    background-image: linear-gradient(-90deg, rgba(151,225,95,1) 0%, rgba(1,217,165,1) 100%);
}

</style>