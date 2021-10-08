<template>
    <section class="overflow-hidden">
        <div class="fluid-container pe-5">
            <div class="row justify-content-between">
                <div class="col-lg-5 col-11">
                    <div class=" double-foto-box">
                        <div class="cover"></div>
                        <div class="box-img">
                            <img src="../../assets/businesswoman-analysing-document-P8WSNMC-1024x820.jpg" alt="">
                        </div>
                            
                    </div>
                </div>
                <div class="col-4 me-5">
                    <h1>Learn more about our <span>mission</span></h1>
                    <Spacer />
                    <p class="mt-5 mb-5">Far far away, behind the word mountains, far from the countries Vokalia and Consonantia, there live the blind text. Separated they live in Bookmarksgrove right at the cost of the Semantics, a large language ocean. Separated the live in Bookmarksgrove.</p>
                    <Button :btnElement="msg"/>
                </div> 
            </div>  
        </div>
    </section>
</template>

<script>
import Button from '../Button/primaryButton'
import Spacer from '../Button/spacer'
export default {
    name: 'sectionThree',
    components: {
        Button,
        Spacer,
    },
    data(){
        return{
            msg: 'READ MORE'
        }
    }

}
</script>

<style lang="scss" scoped>
@import '../variables/color';


section{
    background-color: $bgPrimary;
    padding-top: 150px;
    padding-bottom: 300px;

    h1{
        font-size: 2.8rem;
    }

    p{
        font-family: dosis;
        color: $textPrimary;
        font-size: 1rem;
    }

    .double-foto-box{
        position: relative;
        height: 500px;
        background-image: url(../../assets/busy-architect-PYVKWM4-1024x872.jpg);
        background-size: cover;
        background-repeat: no-repeat;
        background-position: center;
        border-top-right-radius: 40px;
        border-bottom-right-radius: 40px;

        .cover{
            position: absolute;
            inset: 0 0 0 0;
            background-image: $gradientGreen;
            opacity: .9;
            border-top-right-radius: 40px;
        }

        .box-img{
            position: absolute;
            border-radius: 20px;
            overflow: hidden;
            box-shadow: 7px 7px 20px rgba(0,0,0,.3);
            top: 80px;
            left: 80px;
            height: 100%;
            width: 100%;

            img{
                width: 100%;
                height: 100%;
                object-fit: cover;
            }
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