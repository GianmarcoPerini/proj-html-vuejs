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
                        <h1>Lets Talk About Work</h1>
                        <Button class="mt-5" :btnElement="msg" />
                    </div>
                </div>
            </div>
        </div>
    </section>
</template>

<script>
import Button from '../Button/secondaryButton'
export default {
    name: 'sectionSeven',
    components: {
        Button,
    },

    data(){
        return{
            msg: 'START NOW'
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
    border-radius: 20px;
    padding: 40px 0;
    color: white;

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