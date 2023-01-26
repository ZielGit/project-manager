<template>
    <div class="row">
        <div class="col s12 m7">
            <CardProject :data="projects" />
        </div>
    </div>
</template>

<script>
import CardProject from './CardProject.vue';

export default {
    data: () => ({
        projects: [],
    }),
    components: { CardProject },
    mounted(){
        this.getProjects();
    },
    methods: {
        async getProjects() {
            const res = await fetch("https://crud-vue-420f8-default-rtdb.firebaseio.com/projects.json")
            const data = await res.json()
            this.projects = data;

            console.log(data);
        },
    }
}
</script>
