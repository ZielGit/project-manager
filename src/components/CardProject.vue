<template>
    <div class="card horizontal">
        <div class="card-stacked">
            <div class="card-content">
                <span class="card-title">{{ data.data.title }}</span>
                <p>{{ data.data.description }}</p>
                <p>Tecnologias: <span v-for="(lang, i) in data.data.langs" :key="i">{{ i < data.data.langs.length - 1 ? `${lang.toUpperCase()}, ` : lang.toUpperCase() }}</span></p>
            </div>
            <div class="row card-action">
                <router-link
                    :to="`/edit-project/${data.id}`"
                    class="col s6 waves-effect waves-light btn amber darken-3"
                >
                    <i class="material-icons">edit</i>
                </router-link>
                <button 
                    @click="deleteProject"
                    class="col s6 waves-effect waves-light btn red darken-3"
                >
                    <i class="material-icons">delete</i>
                </button>
            </div>
        </div>
    </div>
</template>

<script>
export default {
    props: {
        data: Object,
    },
    methods: {
        async deleteProject(){
            const id = this.data.id;
            const res = await fetch(`https://crud-vue-420f8-default-rtdb.firebaseio.com/projects/${id}.json`,
            {
                method: "PATCH",
                body: JSON.stringify({ status: false })
            });
            const data = await res.json();
            this.data.data.status = data["status"];
        }
    }
    // computed: {
    //     lang(){
    //         return this.data.langs
    //     }
    // }
}
</script>