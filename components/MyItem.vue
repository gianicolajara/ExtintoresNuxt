<template>
  <div class="item">
    <div class="item-header">
      <img
        :src="require(`@/assets/images/${item.image}`)"
        alt=""
        class="item-image"
      />
    </div>
    <div class="item-body mt-2 mb-2">
      <h4 class="item-title">
        {{ item.title }}
      </h4>
      <p class="item-snippet text-secondary">
        {{ item.description }}
      </p>
    </div>
  </div>
</template>

<script>
export default {
  props: {
    item: {
      type: Object,
      default: null,
    },
  },
}
</script>

<style scoped>
.item {
  display: flex;
}

.item-header {
  overflow: hidden;
  width: 40%;
  display: flex;
  justify-content: center;
  align-items: center;
}

.item-body {
  width: 60%;
}

.item-image {
  width: 300px;
  height: 200px;
  object-fit: cover;
  border-radius: 1em;
}

.item-title {
  font-weight: 700;
  font-size: 1rem;
}
</style>
