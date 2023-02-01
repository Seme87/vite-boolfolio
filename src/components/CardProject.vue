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
    <img src="..." class="card-img-top" alt="..." />
    <div class="card-body">
      <h5 class="card-title">{{ data.title }}</h5>
      <p class="card-text">
        {{ truncateText(data.description) }}
      </p>
      <a href="#" class="btn btn-primary">Leggi di piu</a>
    </div>
  </div>
</template>

<style lang="scss" scoped></style>
