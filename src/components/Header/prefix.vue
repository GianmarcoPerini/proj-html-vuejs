<template>
    <div class="prefix d-flex justify-content-between align-items-center">
        <div class="d-flex ps-5 text-white pt-2 pb-2">
            <p class="mb-0">{{msg}}</p>
            <p class="ms-4 mb-0">{{tel}}</p>
        </div>
        <div class="pt-2 pb-2 pe-5">
            <i class="text-white fab fa-facebook-f"></i>
            <i class="text-white ms-3 me-3 fab fa-twitter"></i>
            <i class="text-white fab fa-pinterest-p"></i>
        </div>
    </div>
    
</template>

<script>
export default {
    name: 'Prefix',

    data(){
        return{
            msg:'(001) 88451234',
            tel:'88455438',
        }
    },

}
</script>

<style lang="scss" scoped>

div{
    background-color: #3d3d3d;
    p{
        color: #f9f9f9;
        font-size: .8rem;
    }
}

</style>