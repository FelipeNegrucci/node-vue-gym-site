<script setup>
import iconWhatsapp from './icons/iconWhatsapp.vue'
</script>

<template>
    <div class="hero-bg-img container-fluid px-3">
        <div class="container-xxl px-0 h-100">
            <div class="row gx-0 h-100">
                <div class="col vstack gap-4 my-auto user-select-none">
                    <span class="gradient-text display-5 text-uppercase text-center text-md-start">space sport fitness</span>
                    <div class="text-center text-md-start">
                        <span class="h4">Transforme seu corpo e eleve seu potencial</span>
                        <br>
                        <span class="h6">Seja a sua própria inspiração na jornada rumo à sua melhor versão</span>
                    </div>
                    <div class="hstack gap-4 mx-auto mx-md-0 flex-column flex-sm-row">
                        <div class="btn btn-secondary px-4 py-2 rounded-1 d-flex">
                            <span class="my-auto">Fale Conosco</span>
                            <iconWhatsapp class="my-auto ms-2" width="24px" height="24px"/>
                        </div>
                        <div class="btn btn-outline-secondary px-4 py-2 rounded-1">Veja mais</div>
                    </div>
                </div>
            </div>
        </div>
    </div>
</template>

<style scoped>
.hero-bg-img{
    height: 480px;
    background-image:
    linear-gradient(0deg, rgba(43,45,66,0.5) 0%, rgba(43,45,66,0.2) 50%, rgba(43,45,66,0.5) 100%),
        url('../assets/login-workout.jpg');
    background-size: cover;
    background-position: 100% 50%;
}
.gradient-text{
    animation: background-pan 12s linear infinite;
    background: linear-gradient(
        to right,
        #d41f3d,
        #ab69d1,
        #d41f3d,
        #ab69d1,
        #d41f3d
    );
    background-size: 200%;
    background-clip: text;
    -webkit-background-clip: text;
    -webkit-text-fill-color: transparent;
}
@keyframes background-pan{
    from{ background-position: 0% center; }
    to{ background-position: -200% center; }
}
</style>
