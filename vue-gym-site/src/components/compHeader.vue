<script setup>
import iconBrand from './icons/iconBrand.vue'
import iconUser from './icons/iconUser.vue'

import { ref } from 'vue';

const iconSizes = ref({
    brandLogo: '42px',
    acessButton: '20px'
})
</script>

<template>
    <div class="row justify-content-between gx-0 h-100 align-items-center">

        <router-link class="col-auto nav-link" to="/">
            <div class="row gx-0">
                <div class="col-auto">
                    <iconBrand :width="iconSizes.brandLogo" :height="iconSizes.brandLogo"/>
                </div>
                <div class="col-auto ms-2 h5 my-auto text-uppercase">space sport fitness</div>
            </div>
        </router-link>

        <div class="col-auto">
            <div class="row gx-0">
                <div class="col-auto nav gap-3 text-capitalize">
                    <router-link class="nav-link" to="/">sobre</router-link>
                    <router-link class="nav-link" to="/">horários</router-link>
                    <router-link class="nav-link" to="/">contato</router-link>
                </div>
                <div class="col-auto ms-4 my-auto btn btn-primary px-4">
                    <iconUser :width="iconSizes.acessButton" :height="iconSizes.acessButton"/>
                    <span>Acessar</span>
                </div>
            </div>
        </div>

    </div>
</template>

<style scoped>

</style>
