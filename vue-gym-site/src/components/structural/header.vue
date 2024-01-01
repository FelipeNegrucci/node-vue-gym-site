<script setup>
import modalAccountAccess from '../standard/modalAccountAccess.vue'
import compNavigation from '../structural/navigation.vue'
import stdButton from '../standard/button.vue'
import iconBrand from '../icons/iconBrand.vue'
import iconUser from '../icons/iconUser.vue'
import iconToggle from '../icons/iconToggle.vue'

import { ref } from 'vue';

const iconSizes = ref({
    brandLogo: '42px',
    acessButton: '20px'
})

const props = defineProps({
    screenSizeWidth: Number
})

function toggleNavigation() {

}
</script>

<template>
    <modalAccountAccess/>

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
                    <compNavigation/>
                </div>
                <stdButton v-if="props.screenSizeWidth > 830" class="col-auto ms-4 btn-primary" data-bs-toggle="modal" data-bs-target="#modalAccountAccess">
                    <iconUser class="my-auto" :width="iconSizes.acessButton" :height="iconSizes.acessButton"/>
                    <span class="text-capitalize my-auto">acessar</span>
                </stdButton>
                <button v-else @click="toggleNavigation" class="col-auto btn px-0 py-2">
                    <iconToggle aria-expanded="false"/>
                </button>
            </div>
        </div>

    </div>
</template>

<style scoped>

</style>
