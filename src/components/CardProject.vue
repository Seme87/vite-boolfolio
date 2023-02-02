<script>
export default {
  name: "CardProject",
  props: {
    data: Object,
  },
  methods: {
    truncateText(text) {
      return text.substring(0, 180);
    },
  },
};
</script>

<template>
  <div class="card" style="width: 18rem">
    <img :src="data.image_url" class="card-img-top" :alt="data.title" />
    <div class="card-body">
      <h5 class="card-title">{{ data.title }}</h5>
      <p class="card-text">
        {{ truncateText(data.description) }}
      </p>
      <router-link class="btn btn-primary"  :to="{ name: 'single-project', params: {slug:data.slug }  }">Dettagli</router-link>
    
    </div>
  </div>
</template>

<style lang="scss" scoped></style>
