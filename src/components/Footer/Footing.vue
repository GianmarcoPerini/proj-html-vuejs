<template>
    <footer>
        <div class="fluid-container overflow-hidden p-5">
            <div class="row">
                <div class="col-3">
                    <img class="mb-4" src="../../assets/cropped-Group-39-2x.png" alt="">
                    <p>While the lovely valley teems with vapour around me, and the meridian sun strikes the upper surface of the impenetrable foliage of my trees.While the lovely valley teems with vapour around me.</p>
                </div>
                <div class="col-3">
                    
                        <h1>QUICK LINKS</h1>
                        <Spacer />
                        <ul>
                            <li v-for="link in links" :key="link"> <a href="#"> {{link.name}} </a></li>
                        </ul>
                    
                </div>
                <div class="col-3">
                    <h1>CONTACT</h1>
                    <Spacer />
                    <ul>
                        <li class="mt-4 mb-4" v-for="contact in contacts" :key="contact">{{contact.name}}</li>
                    </ul>
                </div>
                <div class="col-3"></div>
            </div>
        </div>
    </footer>
</template>

<script>
import Spacer from '../Button/spacer'


export default {
    name: 'Footing',
    components: {
        Spacer,
    },

    data(){
        return{
            links: [
                {name: 'Careers'},
                {name: 'News'},
                {name: 'Terms of use'},
                {name: 'Privacy projects'},
                {name: 'About'},
                {name: 'Contacts'},
            ],

            contacts: [
                {name: 'Patricia C. Amedee 4401 Waldeck Street Grapevine Nashville, TX 76051'},
                {name: 'info@yourdomain.com'},
                {name: '+99 (0) 101 0000 888'},
            ]
        }
    }

}
</script>

<style lang="scss" scoped>
@import '../variables/color';


    ul{
        list-style: none;
        padding: 0;
    }

    li a,
    li,
    p{
        font-family: dosis;
        color: $textPrimary;
        text-decoration: none;
    }

    li a:hover{
        color: $textActive;
    }


</style>