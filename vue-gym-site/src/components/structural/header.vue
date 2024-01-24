<script setup>
import modalAccountAccess from '../standard/modalAccountAccess.vue'
import compNavigation from '../structural/navigation.vue'
import stdButton from '../standard/button.vue'
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
</script>

<template>
    <modalAccountAccess/>

    <div class="row justify-content-between gx-0 h-100 align-items-center user-select-none px-4">

        <router-link class="col-auto nav-link ms-0 ms-xl-2" to="/">
            <div class="row gx-0">
                <div class="col-auto">
                    <img src="../../assets/brand-logo.png" width="48">
                </div>
                <div v-if="props.screenSizeWidth > 430" class="col-auto ms-2 h5 my-auto text-uppercase text-light">space sport fitness</div>
            </div>
        </router-link>

        <div  class="col-auto me-0 me-xl-2">
            <div class="row gx-0">
                <div v-if="props.screenSizeWidth > 830" class="col-auto nav gap-3 text-capitalize">
                    <compNavigation/>
                </div>
                <stdButton v-if="props.screenSizeWidth > 830" class="col-auto ms-4 btn-primary" data-bs-toggle="modal" data-bs-target="#modalAccountAccess">
                    <iconUser class="my-auto" :width="iconSizes.acessButton" :height="iconSizes.acessButton"/>
                    <span class="text-capitalize my-auto">acessar</span>
                </stdButton>
                <button v-else @click="toggleNavigation" class="col-auto btn px-0 py-2 collapsed" data-bs-toggle="collapse" data-bs-target="#collapseNav" aria-expanded="false" aria-controls="collapseNav">
                    <iconToggle/>
                </button>
            </div>
        </div>

    </div>

    <div class="row collapse w-100 mx-0" id="collapseNav">
        <div class="col-auto nav gap-3 text-uppercase h6 py-4 flex-column mx-auto text-center">
            <compNavigation/>
        </div>
    </div>

</template>

<style scoped>
#collapseNav{
    background: rgb(43,45,66);
    background: linear-gradient(0deg, rgba(43,45,66,0.9) 0%, rgba(43,45,66,0.9) 64%, rgba(43,45,66,0.9) 100%);
    border-bottom: 3px solid rgba(43,45,66,0.3);
}
</style>
