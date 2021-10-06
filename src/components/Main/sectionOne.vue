<template>
    <section class="position-relative">
        <div class="container ">
            <div class="row ">
                <div class="col-7">
                    <p class="subT fw-bold">17 YEARS OF EXPERIENCE</p>
                    <h1 class="fw-bold">We ara a <br> Web Design <span>Agency</span></h1>
                    <div class="spacer d-flex mt-4 mb-4">
                        <div class="spacer-one h-100 w-25 bg-primary me-1"></div>
                        <div class="spacer-two h-100 w-75 bg-primary"></div>
                    </div>                
                    <p class="pt-4 pb-4">Far far away, behind the word mountains, far from the countries Vokalia and Consonantia, there live the blind text. Separated they live in Bookmarksgrove right at the cost of the Semantics, a large language ocean. Separated the live in Bookmarksgrove.</p>
                    <Button class="mb-5" :msg="buttonMsg"/>
                    <div class="pb-5 d-flex align-items-baseline justify-content-between">
                        <p class="fw-bold text-black">FACEBOOK - INSTAGRAM - YOUTUBE - TWITTER</p>
                        <multiButton :btnElements="arrChoise"/>
                    </div>
                </div>
                <div class="col overflow-visible">
                    <div class="box-img h-100 position-absolute">
                        <img src="../../assets/Group-36-2x.png" alt="">
                    </div>
                </div>
            </div>
        </div>

    </section>
</template>

<script>
import Button from '../Button/secondaryButton.vue'
import multiButton from '../Button/multiButton.vue'
export default {
    name: 'sectionOne',
    components: {
        Button,
        multiButton,
    },
    data(){
        return{
            buttonMsg: 'READ MORE',
            arrChoise: ['01','02','03']
        }
    }

}
</script>

<style lang="scss" scoped>
@import '../variables/color';

section{
    // height: 100vh;
    background-color: $bgPrimary;
    z-index: 0;
    padding-top: 150px;
    overflow: hidden;

    .subT{
        letter-spacing: 7px;
        font-size: .7rem;
        color: $textActive;
    }

    p{
        font-family: roboto;
        color: $textPrimary;
        font-size: .9rem;
    }

    h1{
        font-size: 3rem;

        span{
            color: $textActive;
        }
    }
.box-img{
    top: 0;
    width: 60%;
    z-index: -1;

    img{
        // margin-top: 80px;
        width: 100%;
        height: 120%;
        object-fit: contain;
    }
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