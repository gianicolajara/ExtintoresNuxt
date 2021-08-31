<template>
  <NuxtLink :to="`products/${card.id}`" class="card">
    <div class="card-header">
      <img
        :src="require(`@/assets/images/${card.image || 'fe1.jpg'}`)"
        alt=""
        class="card-image"
      />
    </div>
    <div class="card-body">
      <h3 class="header">{{ cardinfo.title }}</h3>
      <p class="snippet text-secondary">{{ cardinfo.snippet }}</p>
    </div>
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
      cardinfo: this.card,
    }
  },
}
</script>

<style scoped>
.card {
  display: flex;
  width: 33.33%;
  border-radius: 5%;
  overflow: hidden;
  text-decoration: none;
}

.header {
  font-size: 1rem;
  color: black;
  font-weight: 700;
}

.snippet {
  font-size: 1rem;
}

.card-image {
  position: absolute;
  width: 100%;
  height: 100%;
  object-fit: cover;
}

.card-header {
  position: relative;
  width: 100%;
  padding: 0;
  height: 200px;
}
</style>
