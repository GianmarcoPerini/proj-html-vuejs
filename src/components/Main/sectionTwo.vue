<template>
    <section class="position-relative">
        <div class="container ">
            <div class="row">
                <div class="col-6">
                    <h1 class="fw-bold">We are Here To<br> Make Your <span>Website</span> <br> Look More <span>Elegant</span> <br> And Stylish!</h1>
                    <div class="spacer d-flex mt-5 mb-5">
                        <div class="spacer-one h-100 w-25 bg-primary me-1"></div>
                        <div class="spacer-two h-100 w-75 bg-primary"></div>
                    </div>
                    <Button :msg="'VIEW ALL'"/>
                </div>
                <div class="col-6">
                </div>
            </div>  
        </div>

    </section>
</template>

<script>
import Button from '../Button/primaryButton.vue'
// import multiButton from '../Button/multiButton.vue'
export default {
    name: 'sectionOne',
    components: {
        Button,
        // multiButton,
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
    background-color: #fff;
    padding-top: 150px;
    overflow-x: hidden;

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
        line-height: 80px;
        font-size: 3rem;

        span{
            color: $textActive;
        }
    }

    .box-img{
        top: 0;
        right: 0;
        height: 90%;
        width: 60%;
        pointer-events: none;
        // background-color: red;
        // overflow: auto;

        img{
            height: 100%;
            width: 100%;
            object-fit: cover;
            position: absolute;
            right: -150px;
            // left: -150px;
            // top: 100px;
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