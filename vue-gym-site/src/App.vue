<script setup>
import compHeader from './components/structural/header.vue'
import compSectionHero from './components/sections/hero.vue'

import { ref, onBeforeMount, onMounted } from 'vue'

const headerHeight = ref('62px')
const widthPadding = ref('px-0 px-md-2 px-xl-3 px-xxl-0')

var screenSize = ref({
    width: null,
    height: null
})

function getScreenSize(){
    return {
        width: window.innerWidth,
        height: window.innerHeight
    }
}

onBeforeMount(()=>{
    screenSize.value = getScreenSize()
})

onMounted(()=>{
        window.addEventListener('resize', () => {
        screenSize.value = getScreenSize()
    });
})
</script>

<template>
    <header class="container-fluid px-3 position-absolute" :style="{ height: headerHeight }">
        <div class="container-xxl px-0 h-100">
            <compHeader :screenSizeWidth="screenSize.width" :widthPadding="widthPadding"/>
        </div>
    </header>
    <main class="container-fluid px-0">
        <compSectionHero class="text-light" :widthPadding="widthPadding" :style="{ paddingTop: headerHeight }"/>
    </main>
    <footer>

    </footer>
</template>

<style lang="scss">
header{
    background: rgb(43,45,66);
    background: linear-gradient(0deg, rgba(43,45,66,0.3) 0%, rgba(43,45,66,0.5) 64%, rgba(43,45,66,0.8) 100%);
    border-bottom: 1px solid rgba(43,45,66,0.3);
}
</style>
