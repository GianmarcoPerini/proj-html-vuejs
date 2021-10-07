<template>
    <section class="overflow-hidden">
        <div class="fluid-container">
            <div class="row">
                <div class="col-lg-5 col-11">
                    <div class=" double-foto-box">
                        <div class="cover"></div>
                        <div class="box-img">
                            <img src="../../assets/businesswoman-analysing-document-P8WSNMC-1024x820.jpg" alt="">
                        </div>
                            
                    </div>
                </div>
                <div class="col-7">
                    <Button :btnElement="msg"/>
                </div> 
            </div>  
        </div>
    </section>
</template>

<script>
import Button from '../Button/primaryButton'
export default {
    name: 'sectionThree',
    components: {
        Button,
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
    padding-bottom: 150px;

    .double-foto-box{
        position: relative;
        height: 500px;
        background-image: url(../../assets/busy-architect-PYVKWM4-1024x872.jpg);
        background-size: cover;
        background-repeat: no-repeat;
        background-position: center;
        border-top-right-radius: 40px;
        border-bottom-right-radius: 40px;
        // overflow: hidden;

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





}
</style>