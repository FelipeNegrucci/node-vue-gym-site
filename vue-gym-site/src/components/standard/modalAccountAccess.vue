<script setup>
</script>

<template>
    <div class="modal fade" id="modalAccountAccess" tabindex="-1" aria-labelledby="exampleModalLabel" aria-hidden="true">
        <div class="modal-dialog modal-dialog-centered">
            <div class="modal-content borde py-4 px-4">
                <div class="modal-body container-fluid text-dark vstack">
                    <div class="row row-cols-1 gx-0 text-center mb-4 user-select-none">
                        <div class="col mx-auto display-6 fs-3 text-uppercase">acesse sua conta</div>
                        <div class="col mx-auto text-secondary fst-italic mt-1">Tenha acesso a sua ficha de treinos e mais.</div>
                    </div>
                    <form class="vstack gap-3">
                        <div class="row">
                            <label for="inputName" class="col-sm-2 col-form-label">Nome</label>
                            <div class="col-sm-10">
                              <input type="text" class="form-control" id="inputName">
                            </div>
                        </div>
                        <div class="row">
                            <label for="inputPassword" class="col-sm-2 col-form-label">Senha</label>
                            <div class="col-sm-10">
                              <input type="password" class="form-control" id="inputPassword">
                            </div>
                        </div>
                        <div class="row mt-2">
                            <button class="col-auto btn px-4 py-2 rounded-1 btn-primary mx-auto" type="submit">
                                <span class="text-uppercase">entrar</span>
                            </button>
                        </div>
                    </form>
                </div>
            </div>
        </div>
    </div>
</template>

<style scoped>

</style>
