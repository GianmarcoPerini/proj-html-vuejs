<template>
    <main>
        <sectionOne />
        <sectionTwo />
        <sectionThree />
        <sectionFour />
    </main>
</template>

<script>
import sectionOne from './sectionOne';
import sectionTwo from './sectionTwo';
import sectionThree from './sectionThree';
import sectionFour from './sectionFour';

export default {
    name: 'mainWrapper',
    components: {
        sectionOne,
        sectionTwo,
        sectionThree,
        sectionFour,
    }

}
</script>

<style lang="scss">
@import '../variables/color';

    span{
        color: $textActive;
    }
</style>