<template>
    <div class="card horizontal">
        <div class="card-stacked">
            <div class="card-content">
                <span class="card-title">{{ data.title }}</span>
                <p>{{ data.description }}</p>
                <p>Tecnologias: <span v-for="(lang, i) in data.langs" :key="i">{{ i < data.langs.length - 1 ? `${lang.toUpperCase()}, ` : lang.toUpperCase() }}</span></p>
            </div>
            <div class="row card-action">
                <router-link
                    to="/reg-projects"
                    class="col s6 waves-effect waves-light btn amber darken-3"
                >
                    <i class="material-icons">edit</i>
                </router-link>
                <a class="col s6 waves-effect waves-light btn red darken-3"><i class="material-icons">delete</i></a>
            </div>
        </div>
    </div>
</template>

<script>
export default {
    props: {
        data: Object,
    },
    computed: {
        lang(){
            return this.data.langs
        }
    }
}
</script>