<template>
    <section>
        <div class="container">
            <div class="row">
                <div class="col-6 text-center">
                    <div class="box black">
                        <p>Are You Ready?</p>
                        <h1>Start a New Project</h1>
                        <input class="w-75 mt-5" type="text" placeholder="Enter your email address">
                    </div>
                </div>
                <div class="col-6 text-center">
                    <div class="box green">
                        <p>What are you waiting for?</p>
                        <h1>Let's Talk About Work</h1>
                        <Button class="mt-5" :btnElement="msg" />
                    </div>
                </div>
                <div class="col-2 d-flex align-items-center" v-for="el in sponsor" :key="el.id">
                    <Sponsor :path="el.path"/>
                </div>
            </div>
        </div>
    </section>
</template>

<script>
import Button from '../Button/primaryButton'
import Sponsor from './sponsor'
export default {
    name: 'sectionSeven',
    components: {
        Button,
        Sponsor
    },

    data(){
        return{
            msg: 'START NOW',

            sponsor: [
                {id: 0, path: 'client-1-2x'},
                {id: 1, path: 'client-9-2x'},
                {id: 2, path: 'client-7-2x'},
                {id: 3, path: 'client-3-2x'},
                {id: 4, path: 'client-4-2x'},
                {id: 5, path: 'client-5-2x'},
            ]
        }
    }

}
</script>

<style lang="scss" scoped>
@import '../variables/color';

section{
    background-color: $bgPrimary;
    padding: 100px;
}

.box{
    border-radius: 15px;
    padding: 40px 0;
    color: white;

    h1{
        font-family: work sans;
        font-style: italic;
        font-weight: bold;
    }

    p{
        font-family: work sans;
        font-style: italic;
        font-weight: 300;
    }

    input{
        padding: 15px 45px;
        border-radius: 50px;
        font-size: .8rem;
        background-color: rgb(63, 63, 63);
        border: none;
        color: rgb(224, 224, 224);
    }
}

.green{
    background-image: $gradientGreen;
    box-shadow: $shadowGreen;
}

.black{
    background-image: $gradientBlack;
    box-shadow: $shadowBlack;
}


</style>