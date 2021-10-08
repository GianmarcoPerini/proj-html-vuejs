<template>
    <div class="button d-flex align-items-center">
        <div class="single-button"  @click="goTo(i), changeImage(dataChoise[indexCount].path, dataChoise[indexCount].text, dataChoise[indexCount].highlight, i)" v-for="(el, i) in dataChoise" :key="el.id"  :class="(i == indexCount) ? 'active' : '' " > {{el.id}} </div>
    </div>
</template>

<script>
export default {
    name:'multiButton',
    props: {
        dataChoise: Array,
        
        changeImage: {
            id: String,
            path: String,
        },
    },

    data(){
        return{
            indexCount: 0,
            path: '',
        }

        
    },

    methods:{
        goTo(index){
            this.indexCount = index
        },

    },

    created(){
        setInterval(()=>{
            this.indexCount++
            if(this.indexCount >= this.dataChoise.length) this.indexCount = 0
        },8000)
    }
}
</script>

<style lang="scss" scoped>
@import '../variables/color';

.button{
    background-image: $gradientBlack;
    border-radius: 25px;
}
.single-button{
    padding: 9px 15px;
    border-radius: 20px;
    margin: 4px;
    color: $textLight;
    cursor: pointer;

    &:hover{
        color: $textActive;
    }
}

.active{
    background-image: $gradientGreen;
}

</style>