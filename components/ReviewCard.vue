<template>
  <div class="review">
    <div class="review-header">
      <img :src="person.picture.large" alt="" class="review-image" />
    </div>
    <div class="review-body mt-2 mb-2">
      <h4 class="review-title">
        {{ person.login.username }}
      </h4>
      <p class="review-snippet text-secondary">
        Lorem ipsum, dolor sit amet consectetur adipisicing elit. Quasi id
        incidunt perferendis excepturi ipsum. Excepturi natus in pariatur fugit
        nemo, temporibus aperiam debitis incidunt nesciunt! Similique blanditiis
        numquam voluptas vero.
      </p>
    </div>
  </div>
</template>

<script>
export default {
  props: {
    person: {
      type: Object,
      default: null,
    },
  },
}
</script>

<style scoped>
.review {
  display: flex;
}

.review-header {
  overflow: hidden;
  width: 15%;
  display: flex;
  justify-content: center;
  align-items: center;
}

.review-body {
  width: 85%;
}

.review-image {
  width: 100px;
  border-radius: 50%;
}

.review-title {
  font-weight: 700;
  font-size: 1rem;
}
</style>
