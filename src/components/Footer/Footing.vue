<template>
    <footer>
        <div class="fluid-container overflow-hidden p-5">
            <div class="row">
                <div class="col-3">
                    <img class="mb-4" src="../../assets/cropped-Group-39-2x.png" alt="">
                    <p>While the lovely valley teems with vapour around me, and the meridian sun strikes the upper surface of the impenetrable foliage of my trees.While the lovely valley teems with vapour around me.</p>
                </div>
                <div class="col-3">
                    
                        <h4>QUICK LINKS</h4>
                        <Spacer />
                        <ul>
                            <li v-for="(link, i) in links" :key="i"> <a href="#"> {{link.name}} </a></li>
                        </ul>
                    
                </div>
                <div class="col-3">
                    <h4>CONTACT</h4>
                    <Spacer />
                    <ul>
                        <li class="mt-4 mb-4" v-for="(contact, i) in contacts" :key="i">{{contact.name}}</li>
                    </ul>
                </div>
                <div class="col-3">
                    <h4>LOCATION ON MAP</h4>
                    <Spacer />
                    <img src="../../assets/map.png" alt="">
                </div>
            </div>
        </div>

        <div class="p-5 d-flex justify-content-between foot">
            <div>
                <p class="m-0">© 2021 PHLOX BUSINESS THEME.</p>
            </div>

            <div>
                <i class="fab fa-facebook-f"></i>
                <i class="fab fa-twitter ms-4 me-4"></i>
                <i class="fab fa-pinterest-p"></i>
            </div>
        </div>
        <a href="#"><div class="to-the-top position-fixed"><i class="fas fa-arrow-up text-dark"></i></div></a>
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

    .to-the-top{
        z-index: 10;
        bottom: 30px;
        right: 10px;
        padding: 20px;
        height: 30px;
        width: 30px;
        display: flex;
        justify-content: center;
        align-items: center;
        background-color: white;
        border: 1px solid black;
        border-radius: 20px;

        i{
            color: yellow;
        }
    }


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

    .foot{
        background-color: $bgFoot;
        
        

        p{
            color: $textLight;
            text-transform: lowercase;
        }

        i{
            color: $textLight;
        }
    }


</style>