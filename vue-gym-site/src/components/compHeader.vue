<script setup>
import buttonMedium from './buttonMedium.vue'
import compAccountAccess from './compAccountAccess.vue'
import iconBrand from './icons/iconBrand.vue'
import iconUser from './icons/iconUser.vue'
import iconToggle from './icons/iconToggle.vue'

import { ref } from 'vue';

const iconSizes = ref({
    brandLogo: '42px',
    acessButton: '20px'
})

const props = defineProps({
    screenSizeWidth: Number
})
</script>

<template>
    <compAccountAccess/>

    <div class="row justify-content-between gx-0 h-100 align-items-center user-select-none">

        <router-link class="col-auto nav-link" to="/">
            <div class="row gx-0">
                <div class="col-auto">
                    <iconBrand :width="iconSizes.brandLogo" :height="iconSizes.brandLogo"/>
                </div>
                <div v-if="props.screenSizeWidth > 430" class="col-auto ms-2 h5 my-auto text-uppercase text-light">space sport fitness</div>
            </div>
        </router-link>

        <div  class="col-auto">
            <div class="row gx-0">
                <div v-if="props.screenSizeWidth > 830" class="col-auto nav gap-3 text-capitalize">
                    <router-link class="nav-link" to="/">sobre</router-link>
                    <router-link class="nav-link" to="/">horários</router-link>
                    <router-link class="nav-link" to="/">contato</router-link>
                </div>
                <buttonMedium v-if="props.screenSizeWidth > 830" class="col-auto ms-4 btn-primary" data-bs-toggle="modal" data-bs-target="#modalAccountAccess">
                    <iconUser class="my-auto" :width="iconSizes.acessButton" :height="iconSizes.acessButton"/>
                    <span class="text-capitalize my-auto">acessar</span>
                </buttonMedium>
                <button v-else class="col-auto btn p-0 rounded-0">
                    <iconToggle aria-expanded="false"/>
                </button>
            </div>
        </div>

    </div>
</template>

<style scoped>

</style>
