<script setup>
import buttonMedium from '../standard/button.vue'
import iconWhatsapp from '../icons/iconWhatsapp.vue'
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
                        <buttonMedium class="btn-secondary d-flex">
                            <span class="my-auto">Fale Conosco</span>
                            <iconWhatsapp class="my-auto ms-2" width="24px" height="24px"/>
                        </buttonMedium>
                        <buttonMedium class="btn-outline-secondary">
                            <span class="my-auto">Veja Mais</span>
                        </buttonMedium>
                    </div>
                </div>
            </div>
        </div>
    </div>
</template>

<style scoped>
.hero-bg-img{
    height: 520px;
    background-image:
    linear-gradient(0deg, rgba(43,45,66,1) 0%, rgba(43,45,66,0.7) 10%, rgba(43,45,66,0.5) 15%, rgba(43,45,66,0.2) 50%, rgba(43,45,66,0.5) 100%),
        url('../../assets//login-workout.jpg');
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
