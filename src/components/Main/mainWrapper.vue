<template>
    <main>
        <sectionOne />
        <sectionTwo />
    </main>
</template>

<script>
import sectionOne from './sectionOne';
import sectionTwo from './sectionTwo';

export default {
    name: 'mainWrapper',
    components: {
        sectionOne,
        sectionTwo,
    }

}
</script>

<style>

</style>