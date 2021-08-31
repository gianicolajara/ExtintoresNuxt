<template>
  <div class="container">
    <h4 class="title">{{ cardinfo.title }}</h4>
    <p class="snippet text-secondary">
      {{ cardinfo.snippet }}
    </p>
    <div class="container-card">
      <LargeCard
        v-for="largeCard in cardinfo.cards"
        :key="largeCard.id"
        :card="largeCard"
      />
    </div>
  </div>
</template>

<script>
import LargeCard from './LargeCard.vue'
export default {
  components: { LargeCard },
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
.title {
  font-weight: 900;
}

.container-card {
  display: flex;
  gap: 1rem;
}

.container {
  margin-top: 2.5em;
  margin-bottom: 2.5em;
}
</style>
