<template>
    <div class="container">
        <h1> {{ project.title}} </h1>
        <img :src="project.image_url" :alt=" project.title">
        <h3>{{ project.description }}</h3>
    </div>
    
</template>

<script>
import axios from 'axios';

    export default {
        name: 'SinglePost',
        data() {
            return {
                project:null
            }
        },
        created() {
           axios
           .get(`http://127.0.0.1:8000/api/projects/${ this.$route.params.slug }`)
           .then((response) => {
            this.project = response.data;
           });
        },
};
</script>

<style lang="scss" scoped>

</style>