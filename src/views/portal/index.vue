<template>
     <div id="index">
       
            <Header/>
            <
     </div>      
     
</template>

<script>
import logo from '../common/logo.vue';
import Header from '../common/Header.vue';
import Home from '../common/home.vue';
export default {
    name: '',
    data: () => ({}),
    components: {
        logo,
        Header,
        'home-app': Home
    },
    methods: {}
};
</script>

<style lang="scss" scoped>

    #index{
        width: 100%;
        max-width: 100%;
    }


</style>