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
            // arrChoise: [
            //     {id: '01', path: "https://demo.phlox.pro/business-2/wp-content/uploads/sites/57/2018/05/Group-36@2x.png", text:'Focus on your ' , highlight: 'Business',},
            //     {id: '02', path: "https://demo.phlox.pro/business-2/wp-content/uploads/sites/57/2018/05/Group-35@2x.png", text:'We are a Web Design ', highlight: 'Agency',},
            //     {id: '03', path: "https://demo.phlox.pro/business-2/wp-content/uploads/sites/57/2018/05/Group-40@2x.png", text:'A group of Expert ', highlight: 'Planner',},
            // ],

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
        },5000)
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
}

.active{
    background-image: $gradientGreen;
}

</style>