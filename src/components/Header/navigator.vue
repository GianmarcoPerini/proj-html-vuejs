<template>
    <nav class="d-flex align-items-baseline justify-content-between p-4">
        <div>
            <img src="../../assets/cropped-Group-39-2x.png" alt="">
        </div>
        <div>
            <ul class="d-flex">
                <li class="pb-3" v-for="(el, i) in menu" :key="i" :class="(i == indexCount) ? 'active' : '' " @click="goTo(i)" > <a href="#"> {{el.objTitle}} </a></li>
            </ul>
        </div>
        <div>
            <Button />
            <i class="fas fa-search ms-4 fs-4"></i>
        </div>
    </nav>
</template>

<script>
import Button from '../button'
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

nav{

    ul{
        list-style: none;
        
        li{
            margin: 0 10px;

            a{
                text-decoration: none;
                color: #555555;
                font-size: .85rem;
            }
        }
    }

    i{
        color: rgba(1,217,165,1);

        &:hover{
            color: rgba(61,61,61,1);
        }
    }

    .active{
        border-bottom: 1px solid black;
    }
}


</style>