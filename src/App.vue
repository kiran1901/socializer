<script setup>
import { RouterLink, RouterView } from 'vue-router'
import HelloWorld from './components/HelloWorld.vue'
import TheHeader from './components/AppHeader.vue'
</script>

<template>
    <div id="socializer-app">
        
        <TheHeader /> 

        <div class="app__loading">
            <loader v-show="loadingCount" />
        </div>
    </div>

    <!-- <img alt="Vue logo" class="logo" src="@/assets/logo.svg" width="125" height="125" /> -->

        <!-- <div class="wrapper">
        <HelloWorld msg="You did it!" />

        
        </div> -->
        <!-- <nav>
            <RouterLink to="/">Home</RouterLink>
            <RouterLink to="/about">About</RouterLink>
        </nav> -->

    <!-- <RouterView /> -->
</template>

<style lang="scss">

</style>
