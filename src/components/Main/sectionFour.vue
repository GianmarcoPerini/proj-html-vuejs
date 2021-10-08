<template>
    <section>
        <div class="fluid-container overflow-hidden ps-3 pe-3">
            <div class="row justify-content-between">
                <div class="col-md-6 col-10">
                    <Spacer />
                    <h1>Our recent <span>web design</span> & some example of past <span>project</span></h1>
                    <Spacer />
                </div>
                <div class="col-md-6 col-10">
                    <p class="mt-5 mb-5">Far far away, behind the word mountains, far from the countries Vokalia and Consonantia, there live the blind text. Separated they live in Bookmarksgrove right at the cost of the Semantics, a large language ocean. Separated the live in Bookmarksgrove.</p>
                </div>
            </div>
        </div>
        
        <div class="fluid-container overflow-hidden mt-5 pb-5 ps-3 pe-3">
            <div class="row g-1">
                <div class="col-lg-3 col-sm-6 col-12" v-for="card in cards" :key="card.id">
                    <imgCards :path="card.path"/>
                </div>
            </div>
        </div>
        <Button class="button d-block m-auto" :btnElement="msg"/>
    </section>
</template>

<script>
import Spacer from '../Button/spacer'
import Button from '../Button/primaryButton.vue'
import imgCards from './imgCards'

export default {
    name: 'sectionFour',
    components: {
        Spacer,
        imgCards,
        Button,
    },
    data(){
        return{
            cards: [
                {id: 0, path: 'ina-soulis-227104-unsplash-1024x1024'},
                {id: 1, path: 'sunisa-misa-531163-unsplash-1024x1024'},
                {id: 2, path: '355H-1024x1024'},
                {id: 3, path: 'photo-1448932252197-d19750584e56-1024x1024'},
                {id: 4, path: 'business-competition-PB366D8-1024x1024'},
                {id: 5, path: 'cozy-sofa-in-living-room-PQR5AB9-1024x1024'},
                {id: 6, path: 'aa9a4539-PQGJ7HU-1024x1024'},
                {id: 7, path: 'cody-davis-253928-unsplash-1024x1024'},
            ],
            msg: 'READ MORE'
        }
    }
}
</script>

<style lang="scss" scoped>
@import '../variables/color';

section{
    padding: 100px 0 150px 0;
}

    p{
        font-family: roboto;
        color: $textPrimary;
        font-size: .9rem;
    }
</style>