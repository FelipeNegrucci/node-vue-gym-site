<script setup>
import compHeader from './components/compHeader.vue'

import { ref } from 'vue';

const headerHeight = ref('48px')
</script>

<template>
    <header class="container-fluid px-3 text-bg-dark" :style="{ height: headerHeight }">
        <div class="container-xxl px-0 h-100">
            <compHeader/>
        </div>
    </header>
    <main>

    </main>
    <footer>

    </footer>
</template>

<style lang="scss">

</style>
