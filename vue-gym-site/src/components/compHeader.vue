<script setup>
import buttonMedium from './buttonMedium.vue'
import iconBrand from './icons/iconBrand.vue'
import iconUser from './icons/iconUser.vue'

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
    <div class="row justify-content-between gx-0 h-100 align-items-center user-select-none">

        <router-link class="col-auto nav-link" to="/">
            <div class="row gx-0">
                <div class="col-auto">
                    <iconBrand :width="iconSizes.brandLogo" :height="iconSizes.brandLogo"/>
                </div>
                <div class="col-auto ms-2 h5 my-auto text-uppercase">space sport fitness</div>
            </div>
        </router-link>

        <div  class="col-auto">
            <div class="row gx-0">
                <div v-if="props.screenSizeWidth > 830" class="col-auto nav gap-3 text-capitalize">
                    <router-link class="nav-link" to="/">sobre</router-link>
                    <router-link class="nav-link" to="/">horários</router-link>
                    <router-link class="nav-link" to="/">contato</router-link>
                </div>
                <buttonMedium v-if="props.screenSizeWidth > 630" class="col-auto ms-4 btn-primary d-flex" data-bs-toggle="modal" data-bs-target="#exampleModal">
                    <iconUser class="my-auto" :width="iconSizes.acessButton" :height="iconSizes.acessButton"/>
                    <span class="text-capitalize my-auto">acessar</span>
                </buttonMedium>
            </div>
        </div>

        <div class="modal fade" id="exampleModal" tabindex="-1" aria-labelledby="exampleModalLabel" aria-hidden="true">
            <div class="modal-dialog modal-dialog-centered">
                <div class="modal-content">
                    <div class="modal-body container-fluid text-dark vstack gap-4 p-5">
                        <div class="row gx-0 mb-2 mx-auto gap-2">
                            <div class="col-auto btn btn-light px-4 py-3 disabled" aria-disabled="true">acessar conta</div>
                            <div class="col-auto btn btn-light px-4 py-3">nova conta</div>
                        </div>
                        <div class="row row-cols-1 gx-0 text-center">
                            <div class="col mx-auto display-6 fs-3 text-uppercase">acesse sua conta</div>
                            <div class="col mx-auto h6 text-secondary">Tenha acesso a sua ficha de treinos e mais.</div>
                        </div>
                        <form class="row gx-0">
                            <div class="col-12">
                                <label for="inputAccountName" class="form-label text-secondary">nome</label>
                                <input type="text" class="form-control" id="inputAccountName">
                            </div>
                            <div class="col-12 mt-2">
                                <label for="inputPassword" class="form-label text-secondary">senha</label>
                                <input type="text" class="form-control" id="inputPassword">
                            </div>
                            <button class="col-7 mt-5 btn btn-primary mx-auto py-3 text-uppercase" type="submit">
                                enviar
                            </button>
                        </form>
                    </div>
                </div>
            </div>
        </div>

    </div>
</template>

<style scoped>

</style>
