<template>
    <section class="position-relative">
        <div class="container ">
            <div class="row">
                <div class="col-6">
                    <p class="fw-bold">17 YEARS OF EXPERIENCE</p>
                    <h1 class="fw-bold">We ara a <br> Web Design <span>Agency</span></h1>
                </div>
                <div class="col-6">
                    <div class="box-img position-absolute"></div>
                    <!-- <img class="h-100" src="../../assets/Group-36-2x.png" alt=""> -->
                </div>
            </div>
        </div>
    </section>
</template>

<script>
export default {

}
</script>

<style lang="scss">
@import '../variables/color';

section{
    // height: 100vh;
    background-color: $backgroundPrimary;
    padding-top: 150px;

    p{
        letter-spacing: 7px;
        font-size: .9rem;
        color: $textActive;
    }

    h1{
        font-size: 3rem;

        span{
            color: $textActive;
        }
    }

    .box-img{
        top: 0;
        right: 0;
        height: 100%;
        width: 50%;
        background-color: red;
    }

    
}

</style>