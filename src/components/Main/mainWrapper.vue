<template>
    <main>
        <sectionOne />
        <sectionTwo />
        <sectionThree />
        <sectionFour />
        <sectionFive />
        <sectionSix />
        <sectionSeven />
    </main>
</template>

<script>
import sectionOne from './sectionOne';
import sectionTwo from './sectionTwo';
import sectionThree from './sectionThree';
import sectionFour from './sectionFour';
import sectionFive from './sectionFive';
import sectionSix from './sectionSix';
import SectionSeven from './sectionSeven';

export default {
    name: 'mainWrapper',
    components: {
        sectionOne,
        sectionTwo,
        sectionThree,
        sectionFour,
        sectionFive,
        sectionSix,
        SectionSeven,

    }

}
</script>

<style lang="scss">
@import '../variables/color';

    span{
        color: $textActive;
    }
</style>