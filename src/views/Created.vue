<template>
    <div class="container">
        <div class="row">
            <router-link
                to="/proyectos"
                class="col s12 waves-effect waves-light btn amber darken-3"
            >
                <i class="material-icons">arrow_back</i>
                Regresar a la lista
            </router-link>
        </div>
        <div class="row">
            <form @submit.prevent="createProject" class="col s12">
                <div class="row">
                    <div class="input-field col s12">
                        <input id="first_name" type="text" v-model="project.title" class="validate">
                        <label for="first_name">Nombre del Proyecto</label>
                    </div>
                    <div class="input-field col s12">
                        <input id="last_name" type="text" v-model="project.description" class="validate">
                        <label for="last_name">Descripción del Proyecto</label>
                    </div>
                    <p>
                        <label>
                            <input type="checkbox" v-model="project.langs" value="html" checked="checked" />
                            <span>HTML</span>
                        </label>
                    </p>
                    <p>
                        <label>
                            <input type="checkbox" v-model="project.langs" value="css" checked="checked" />
                            <span>CSS</span>
                        </label>
                    </p>
                    <p>
                        <label>
                            <input type="checkbox" v-model="project.langs" value="javascript" checked="checked" />
                            <span>JavaScript</span>
                        </label>
                    </p>
                    <p>
                        <label>
                            <input type="checkbox" v-model="project.langs" value="vue" checked="checked" />
                            <span>Vue</span>
                        </label>
                    </p>
                    <button class="btn waves-effect waves-light col s12" type="submit" name="action">Submit
                        <i class="material-icons right">send</i>
                    </button>
                </div>
            </form>
        </div>
    </div>
</template>

<script>
export default {
    data () {
        return {
            project: {
                title: "",
                description: "",
                langs: [],
                status: true
            }
        }
    },
    methods: {
        async createProject() {
            console.log(this.project);
            // await fetch("https://crud-vue-420f8-default-rtdb.firebaseio.com/projects.json",
            // {
            //     method: "POST",
            //     body: JSON.stringify(this.project),
            // });
        },
    }
}
</script>