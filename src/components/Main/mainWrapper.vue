<template>
    <main>
        <sectionOne />
        <sectionTwo />
        <sectionThree />
        <sectionFour />
        <sectionFive />
    </main>
</template>

<script>
import sectionOne from './sectionOne';
import sectionTwo from './sectionTwo';
import sectionThree from './sectionThree';
import sectionFour from './sectionFour';
import sectionFive from './sectionFive';

export default {
    name: 'mainWrapper',
    components: {
        sectionOne,
        sectionTwo,
        sectionThree,
        sectionFour,
        sectionFive,
    }

}
</script>

<style lang="scss">
@import '../variables/color';

    span{
        color: $textActive;
    }
</style>