<template>
    <section>
        <div class="d-flex align-items-center flex-column">
            <h1>Latest news & our <span>Blog</span></h1>
            <Spacer class="mt-5" />
        </div>

        <div class="container">
            <div class="row">
                <div class="col-md-4 col-12" v-for="card in cards" :key="card.id">
                    <Cards class="mb-5" :date="date" :path="card.path" :text="card.text" :creator="card.creator"/>
                </div>
                
            </div>
            
        </div>
        <Button class="d-block m-auto mt-5" :btnElement="msg"/>
    </section>
</template>

<script>
import Button from '../Button/secondaryButton'
import Spacer from '../Button/spacer'
import Cards from './descriptiveCards'
import date from 'date-and-time'
export default {
    name: 'sectionSix',
    components: {
        Spacer,
        Cards,
        Button,
    },

    data(){
        return{
            msg: 'VIEW ALL POST',
            date: '',
            cards: [
                {id: 0, path: 'serious-businesswoman-with-documents-talking-on-P9Q6LX6-1024', text: 'Marketing ideas', creator: '-by Alex' },
                {id: 1, path: 'Businessman-at-the-desk-in-his-office-resting--1024x768', text: 'Rest during working hour', creator: '-by Alex'},
                {id: 2, path: 'simple-home-office-with-tree-PBXRXYB-large-1024x768', text: 'Develop your start-up ideas', creator: '-by Alex'},
            ]
        }
    },

    mounted(){
        const now = date.format(new Date(), 'DD-MMM-YYYY'); 
        this.date = now
    }

}
</script>

<style lang="scss" scoped>
@import '../variables/color';

section{
    padding-top: 150px;
    padding-bottom: 150px;
    background-color: $bgPrimary;
}

</style>