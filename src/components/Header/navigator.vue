<template>
    <div class="fluid-container overflow-hidden pt-4 pe-4 ps-4">
        <div class="row justify-content-between">
            <div class="col-md-3 col-12 img-box">
                <img class="d-block m-auto" src="../../assets/cropped-Group-39-2x.png" alt="">
            </div>
            <div class="col-lg-6 col-md-8 col-12 text-center mt-sd-0 mt-2">
                <ul class="m-0 p-0">
                    <li class="d-inline-block pb-4" v-for="(el, i) in menu" :key="i" :class="(i == indexCount) ? 'active' : '' " @click="goTo(i)" ><a href="#"> {{el.objTitle}}</a></li>
                </ul>
            </div>
            <div class="col-lg-3 co col-12  d-flex align-items-center justify-content-end">
                <Button class="button" :btnElement="msg"/>
                <i class="fas fa-search ms-4 fs-4"></i>
            </div>
        </div>
        
    </div>
    
    
</template>

<script>
import Button from '../Button/primaryButton.vue'
export default {
    name: 'Navigator',
    components: {
        Button,
    },

    data(){
        return{
            menu: [
                { objTitle: 'HOME' },
                { objTitle: 'ABOUT' },
                { objTitle: 'SERVICES' },
                { objTitle: 'SHOWCASE' },
                { objTitle: 'BLOG' },
                { objTitle: 'CONTACTS' },
            ],
            msg: 'PURCHASE',
            indexCount: 2
        }
    },

    methods: {
        goTo(index){
            this.indexCount = index
        }
    }
}
</script>

<style lang="scss" scoped>
@import '../variables/color';



    .img-box{
        // width: 200px;

        img{
            width: 70%;
        }
    }

    ul{
        list-style: none;
        
        li{
            margin: 0 10px;

            a{
                text-decoration: none;
                color: $textPrimary;
                font-size: .85rem;
            }
        }
    }

    i{
        color: $textActive;
        transition: 200ms;
        cursor: pointer;

        &:hover{
            color: rgba(61,61,61,1);
        }
    }

    .active{
        border-bottom:3px solid rgba(1,217,165,1);
    }

@media screen and (max-width: 992px) {
    .button,
    i {
        display: none;
    }
}

</style>