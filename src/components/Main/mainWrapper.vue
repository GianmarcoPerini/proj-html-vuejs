<template>
    <main>
        <sectionOne />
        <sectionTwo />
        <sectionThree />
    </main>
</template>

<script>
import sectionOne from './sectionOne';
import sectionTwo from './sectionTwo';
import sectionThree from './sectionThree';

export default {
    name: 'mainWrapper',
    components: {
        sectionOne,
        sectionTwo,
        sectionThree,
    }

}
</script>

<style lang="scss">
@import '../variables/color';

    span{
        color: $textActive;
    }
</style>