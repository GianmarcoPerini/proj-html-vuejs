<template>
    <section class="position-relative">
        <div class="container ">
            <div class="row ">
                <div class="col-lg-7 col-11">
                    <p class="subT fw-bold">17 YEARS OF EXPERIENCE</p>
                    <!-- testo dinamico -->
                    <h1 class="col-lg-8 col-10 fw-bold">{{images[index].text}}<span>{{images[index].highlight}}</span></h1>
                    <Spacer />               
                    <p class=" col-lg-8 col-10 pt-4 pb-4">Far far away, behind the word mountains, far from the countries Vokalia and Consonantia, there live the blind text. Separated they live in Bookmarksgrove right at the cost of the Semantics, a large language ocean. Separated the live in Bookmarksgrove.</p>
                    <Button class="mb-5" :btnElement="msg"/>
                    <div class="pb-5 d-flex align-items-baseline justify-content-between">
                        <p class="fw-bold text-black">FACEBOOK - INSTAGRAM - YOUTUBE - TWITTER</p>
                        <multiButton class="d-none d-lg-flex" :dataChoise="images"/>
                    </div>
                </div>
                <!-- slideShow -->
                <div class="box-img d-none d-lg-block"><img :src=" require('../../assets/' + images[index].path + '.png') " alt=""></div>

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
            images: [
                {id: '01', path: "Group-35-2x", text:'Focus on your ' , highlight: 'Business',},
                {id: '02', path: "Group-36-2x", text:'We are a Web Design ', highlight: 'Agency',},
                {id: '03', path: "Group-40-2x", text:'A group of Expert ', highlight: 'Planner',},
            ],
        }
    },

    mounted(){
        setInterval(()=>{
            this.index++
            if(this.index >= this.images.length) this.index = 0
        },8000)
    }
}
</script>

<style lang="scss" scoped>
@import '../variables/color';

section{
    background-color: $bgPrimary;
    z-index: 1;
    padding: 100px 0;
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
        right: -50%;
        height: 100%;
        width: 100%;
        pointer-events: none;
        z-index: -1;

        img{
            height: 100%;
        }
    }
}

</style>