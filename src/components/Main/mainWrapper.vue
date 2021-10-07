<template>
    <main>
        <sectionOne />
        <sectionTwo />
        <sectionThree />
        <sectionFour />
        <sectionFive />
        <sectionSix />
    </main>
</template>

<script>
import sectionOne from './sectionOne';
import sectionTwo from './sectionTwo';
import sectionThree from './sectionThree';
import sectionFour from './sectionFour';
import sectionFive from './sectionFive';
import sectionSix from './sectionSix';

export default {
    name: 'mainWrapper',
    components: {
        sectionOne,
        sectionTwo,
        sectionThree,
        sectionFour,
        sectionFive,
        sectionSix,
    }

}
</script>

<style lang="scss">
@import '../variables/color';

    span{
        color: $textActive;
    }
</style>