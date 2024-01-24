<script>

import AppHeader from './components/AppHeader.vue';
import AppJumbotron from './components/AppJumbotron.vue';
import AppMain from './components/AppMain.vue';
import AppFooter from './components/AppFooter.vue';



export default {
    data() {
        return {
             
        };
     },

    components: {
        AppHeader,
        AppJumbotron,
        AppMain,
        AppFooter

    },

    methods: {

    }
}
</script>

<template>

    <AppHeader/>

    <AppJumbotron/>

    <AppMain/>

    <AppProductCard/>

    <AppBlueBar/>

    <AppFooter/>

</template>

<style lang="scss">
    @use "assets/scss/main.scss" as *;
    @import "assets/scss/partials/reset.scss";
</style>
