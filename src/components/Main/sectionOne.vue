<template>
    <section class="position-relative">
        <div class="container ">
            <div class="row ">
                <div class="col-lg-7 col-11">
                    <p class="subT fw-bold">17 YEARS OF EXPERIENCE</p>
                    <h1 class="fw-bold">{{arrChoise[index].text}}<span>{{arrChoise[index].highlight}}</span></h1>
                    <Spacer />               
                    <p class="pt-4 pb-4">Far far away, behind the word mountains, far from the countries Vokalia and Consonantia, there live the blind text. Separated they live in Bookmarksgrove right at the cost of the Semantics, a large language ocean. Separated the live in Bookmarksgrove.</p>
                    <Button class="mb-5" :btnElement="msg"/>
                    <div class="pb-5 d-flex align-items-baseline justify-content-between">
                        <p class="fw-bold text-black">FACEBOOK - INSTAGRAM - YOUTUBE - TWITTER</p>
                        <multiButton class="d-none d-lg-flex" :changeImage="changeImage" :dataChoise="arrChoise"/>
                    </div>
                    <div class="box-img d-none d-lg-block"
                    :style="{backgroundImage: `url(${arrChoise[index].path})`}"></div>
                </div>
            </div>
        </div>

    </section>
</template>

<script>
import Button from '../Button/secondaryButton.vue'
import multiButton from '../Button/multiButton.vue'
import Spacer from '../Button/spacer'
export default {
    name: 'sectionOne',
    components: {
        Button,
        multiButton,
        Spacer
    },
    data(){
        return{
            index: 0,
            msg: 'READ MORE',
            
            arrChoise: [
                {id: '01', path: "https://demo.phlox.pro/business-2/wp-content/uploads/sites/57/2018/05/Group-36@2x.png", text:'Focus on your ' , highlight: 'Business',},
                {id: '02', path: "https://demo.phlox.pro/business-2/wp-content/uploads/sites/57/2018/05/Group-35@2x.png", text:'We are a Web Design ', highlight: 'Agency',},
                {id: '03', path: "https://demo.phlox.pro/business-2/wp-content/uploads/sites/57/2018/05/Group-40@2x.png", text:'A group of Expert ', highlight: 'Planner',},
            ],
        }
    },

    methods: {
        changeImage(path, txt, highlight, index){
            this.path = path
            this.index = index
            this.text = txt
            this.highlight = highlight
        },
    },

    mounted(){
        setInterval(()=>{
            this.index++
            if(this.index >= this.arrChoise.length) this.index = 0
        },5000)
    }

}
</script>

<style lang="scss" scoped>
@import '../variables/color';

section{
    background-color: $bgPrimary;
    z-index: 1;
    padding: 150px 0;
    overflow: hidden;

    .subT{
        letter-spacing: 7px;
        font-size: .7rem;
        color: $textActive;
    }

    p{
        font-family: dosis;
        font-weight: 100;
        color: $textPrimary;
        font-size: 1rem;
    }

    h1{
        font-size: 3rem;
    }
.box-img{
    position: absolute;
    top: 0;
    right: 0px;
    height: 120%;
    width: 800px;
    background-position: 10px -50px ;
    background-size: cover;
    background-repeat: no-repeat;
    pointer-events: none;
    z-index: -1;
}


    .spacer{
        width: 50px;
        height: 5px;
        
        .spacer-one,
        .spacer-two{
            border-radius: 10px;
            background-image: linear-gradient(45deg, rgba(151,225,95,1) 0%, rgba(1,217,165,1) 100%);
        }
    }
}

</style>