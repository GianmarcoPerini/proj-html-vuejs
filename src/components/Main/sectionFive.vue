<template>
    <div class="fluid-container overflow-hidden">
        <div class="row">
            <div class="col-12">
                <div class="bg-img d-flex flex-column align-items-center position-relative justify-content-center">
                    <div class="cover position-absolute"></div>
                    <i class=" pt-5 fs-1 fas fa-quote-left"></i>
                    <p class="w-50 text-center text-white m-5">When it comes to barbequing, there are two main schools of thought for the techniques that you can use. Freshly scrambled eggs with applewood smoked bacon - are amazing!</p>
                    <div class="user-img mb-3">
                        <img class="w-100" src="../../assets/businesswoman-analysing-document-P8WSNMC-1024x820.jpg" alt="">
                    </div>
                    <p class="fw-bold mt-3 mb-1">LISSA DURBIN</p>
                    <p class="text-white pb-3">Client</p>
                </div>
            </div>
        </div>
    </div>
</template>

<script>
export default {
    name: 'sectionFive'

}
</script>

<style lang="scss" scoped>
@import '../variables/color';

.bg-img{
    background-image: url(../../assets/four-businesspeople-in-a-boardroom-with-paperwork-PC4V8H4.jpg);
    background-size: cover;
    background-repeat: no-repeat;
    background-position: center;

    .cover{
        inset: 0 0 0 0;
        background-color: rgba(0, 0, 0, .7);
    }

    .user-img{
        width: 90px;
        height: 90px;
        border-radius: 100%;
        background-color: white;
        z-index: 10;
        overflow-x: hidden;
        border: 3px solid white;
    }

    i{
        color: #00d9a6;
        z-index: 10;;
    }

    p{
        z-index: 10;
        font-family: dosis;
        font-size: 1.5rem;
        color: #00d9a6;
    }
}

</style>