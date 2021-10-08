<template>
    <nav class="d-flex align-items-baseline justify-content-between pt-4 pe-4 ps-4">
        <div class="img-box">
            <img src="../../assets/cropped-Group-39-2x.png" alt="">
        </div>
        <div>
            <ul class="d-flex m-0">
                <li class="pb-4" v-for="(el, i) in menu" :key="i" :class="(i == indexCount) ? 'active' : '' " @click="goTo(i)" ><a href="#"> {{el.objTitle}}</a></li>
            </ul>
        </div>
        <div>
            <Button :btnElement="msg"/>
            <i class="fas fa-search ms-4 fs-4"></i>
        </div>
    </nav>
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

nav{

    .img-box{
        width: 200px;

        img{
            width: 100%;
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
}


</style>