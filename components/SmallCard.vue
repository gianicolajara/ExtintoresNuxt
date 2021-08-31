<template>
  <NuxtLink :to="`/products/${smallcard.id}`" class="image-container">
    <img
      :src="require(`@/assets/images/${smallcard.image || 'fe1.jpg'}`)"
      alt=""
      class="image"
    />
  </NuxtLink>
</template>

<script>
export default {
  props: {
    card: {
      type: Object,
      default: null,
    },
  },
  data() {
    return {
      smallcard: this.card,
    }
  },
}
</script>

<style scoped>
.image-container {
  width: 23%;
  height: 8em;
  border-radius: 0.5em;
  overflow: hidden;
}

.image {
  width: 100%;
  height: 100%;
  object-fit: cover;
}
</style>
