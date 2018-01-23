<template>
    <div class="shop">
        <comHeader></comHeader>
        <comSidebar v-show="sideBarState"></comSidebar>
        <!-- <keep-alive><router-view></router-view></keep-alive> -->
        <router-view></router-view>
    </div>
</template>

<script type="text/ecmascript-6">
    import Vue from 'vue';
    import comHeader from './components/com/header.vue';
    import comSidebar from './components/com/sidebar.vue';
    import 'mint-ui/lib/style.css';
    import MintUI from 'mint-ui';
    import './css/base.scss';

    Vue.use(MintUI);

    export default {
        data() {
            return {}
        },
        components: {
            comHeader: comHeader,
            comSidebar: comSidebar
        },
        computed: {
            sideBarState() {
                return this.$store.getters.getSideBarState
            }
        }
    }
</script>

<style lang="scss" scope>
    // .shop{
    //   transition: all ease 0.5s;
    // }
</style>
