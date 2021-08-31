<template>
  <div class="hero">
    <div class="information-container">
      <h1 class="header">Find you five Extinguiser</h1>
      <p class="snippet text-secondary">
        Lorem ipsum dolor, sit amet consectetur adipisicing elit. Tempora
        sapiente suscipit sint quas accusamus in quos natus consectetur at
        nesciunt, consequatur fuga a deserunt voluptatem error neque accusantium
        voluptas. Ratione.
      </p>
      <b-button pill variant="danger" class="button-hero"
        >Start Looking</b-button
      >
    </div>
    <div class="image-container">
      <img
        src="~assets/svg/extinguisher-svg.svg"
        alt="fire extinguisher"
        class="image"
      />
    </div>
  </div>
</template>

<script>
import { mapState } from 'vuex'
export default {
  computed: {
    ...mapState(['data1', 'data2', 'data3']),
  },
}
</script>

<style scoped>
.header {
  font-weight: 750;
  font-size: 5rem;
}

.hero {
  display: flex;
  padding: 5em 0;
  gap: 3em;
  margin: 0 auto;
}

.information-container {
  display: flex;
  flex-direction: column;
  justify-content: center;
  align-items: flex-start;
  flex-basis: 60%;
}

.image-container {
  display: flex;
  width: 40%;
}

.image {
  width: 100%;
}

.button-hero {
  width: 8em;
  transition: 0.3s all ease;
}

.button-hero:hover {
  width: 15em;
}
</style>
