<template>
    <div>
        <nav>
            <div class="nav-wrapper">
                <RouterLink to="/">Proyectos</RouterLink>
                <a href="#" data-target="mobile-demo" class="sidenav-trigger"><i class="material-icons">menu</i></a>
                <ul class="right hide-on-med-and-down">
                    <li><RouterLink to="/">Home</RouterLink></li>
                    <li><RouterLink to="/about">About</RouterLink></li>
                    <li><RouterLink to="/proyectos" class="waves-effect waves-light btn">Proyectos</RouterLink></li>
                </ul>
            </div>
        </nav>

        <ul class="sidenav" id="mobile-demo">
            <li><RouterLink to="/">Home</RouterLink></li>
            <li><RouterLink to="/about">About</RouterLink></li>
            <li><RouterLink to="/proyectos">Proyectos</RouterLink></li>
        </ul>
    </div>
</template>

<script>
import { RouterLink } from 'vue-router'
export default {
    mounted() {
        M.AutoInit();
    }
}
</script>