<script setup>
import compHeader from './components/compHeader.vue'

import { ref } from 'vue';

const headerHeight = ref('62px')


</script>

<template>
    <header class="container-fluid px-3 position-absolute" :style="{ height: headerHeight }">
        <div class="container-xxl px-0 h-100">
            <compHeader class="text-light"/>
        </div>
    </header>
    <main class="container-fluid px-0">
        
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
