<template>
    <div class="container">
        <h1>Proyectos</h1>
        <hr>
        <div>
            <router-link
                to="/reg-projects"
                class="col s12 waves-effect waves-light btn amber darken-3"
            >
                <i class="material-icons">add</i>
                Crear Proyecto
            </router-link>
        </div>
        <Contenedor />
    </div>
</template>

<script>
import Contenedor from '../components/Contenedor.vue';

export default {
    components: { Contenedor }
}
</script>
