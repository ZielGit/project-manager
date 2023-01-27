<template>
    <div class="container">
        <div class="row">
            <form class="col s12">
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
    }
}
</script>