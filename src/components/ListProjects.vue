<script>
import axios from "axios";
import CardProject from "./CardProject.vue";
export default {
  name: "ListProjects",
  components: {
    CardProject,
  },
  data() {
    return {
      projects: [],
    };
  },
  created() {
    axios.get("http://127.0.0.1:8000/api/projects").then((response) => {
      this.projects = response.data;
    });
  },
};
</script>

<template>
  <section>
    <h2 class="text-center mb-4">Lista dei Progetti</h2>
    <div class="container">
      <div class="row">
        <div class="col-md-4 g-2" v-for="project in projects">
          <CardProject :data="project" />
        </div>
      </div>
    </div>
  </section>
</template>

<style lang="scss" scoped></style>
