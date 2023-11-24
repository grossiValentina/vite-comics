<script>
import AppHeader from './components/AppHeader.vue';
import AppCard from './components/AppCard.vue';
import AppMain from './components/AppMain.vue';
import AppFooter from './components/AppFooter.vue';


export default {
    components: {
        AppHeader,
        AppCard,
        AppMain,
        AppFooter,
        
    }
}

</script>

<template>

  <AppHeader />
  <AppCard />
  <AppMain />
  <AppFooter />

</template>

<style lang="scss">
@use "./style/general.scss";

</style>
