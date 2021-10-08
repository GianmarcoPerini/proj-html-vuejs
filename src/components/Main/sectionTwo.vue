<template>
    <section>
        <div class="fluid-container ps-3 pe-3">
            <div class="row">
                <div class="col-lg-5 col-11">
                    <h1 class="fw-bold">We are Here To<br> Make Your <span>Website</span> <br> Look More <span>Elegant</span> <br> And Stylish!</h1>
                    <Spacer class="mb-5" />
                    <Button :btnElement="msg"/>
                </div>
                <div class="col-7">
                    <div class="row">
                        <div class="col-6 card-wrapper" v-for="(el, i) in cards" :key="i">
                        <Card  :title="el.title" :text="el.text" :icon="el.icon"/>
                    </div>
                    </div>
                    
                </div> 
            </div>  
        </div>
    </section>
</template>

<script>
import Button from '../Button/primaryButton.vue'
import Card from './cards'
import Spacer from '../Button/spacer'
export default {
    name: 'sectionOne',
    components: {
        Button,
        Card,
        Spacer
    },
    data(){
        return{
            msg: 'VIEW ALL',
            arrChoise: ['01','02','03'],
            cards: [
                {
                    title: 'Speed optimization',
                    text: 'Far far away, behind the word mountains, far from the countries Vokalia Separated...',
                    icon: 'fas fa-tachometer-alt'
                },
                {
                    title: 'Website Design',
                    text: 'Far far away, behind the word mountains, far from the countries Vokalia Separated...',
                    icon: 'fas fa-tablet-alt'
                },
                {
                    title: 'Cloud Solution',
                    text: 'Far far away, behind the word mountains, far from the countries Vokalia Separated...',
                    icon: 'fab fa-mixcloud'
                },
                {
                    title: 'Online Marketing',
                    text: 'Far far away, behind the word mountains, far from the countries Vokalia Separated...',
                    icon: 'fas fa-stopwatch'
                },
            ]
        }
    }

}
</script>

<style lang="scss" scoped>
@import '../variables/color';

section{
    background-color: #fff;
    padding-top: 150px;
    padding-bottom: 150px;
    overflow-x: hidden;

    .card-wrapper{
        display: flex;
        flex-wrap: wrap;
    }

    .subT{
        letter-spacing: 7px;
        font-size: .7rem;
        color: $textActive;
    }

    h1{
        line-height: 80px;
        font-size: 2.5rem;
    }

    .box-img{
        top: 0;
        right: 0;
        height: 90%;
        width: 60%;
        pointer-events: none;

        img{
            height: 100%;
            width: 100%;
            object-fit: cover;
            position: absolute;
            right: -150px;
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