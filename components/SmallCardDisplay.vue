<template>
  <div class="container">
    <h3 class="header">{{ data.title }}</h3>
    <div class="card-container">
      <SmallCard
        v-for="smallcard in data.cards"
        :key="smallcard.id"
        :card="smallcard"
      />
    </div>
  </div>
</template>

<script>
import SmallCard from './SmallCard.vue'
export default {
  components: { SmallCard },
  props: {
    card: {
      type: Object,
      default: null,
    },
  },
  data() {
    return {
      data: this.card,
    }
  },
}
</script>

<style scoped>
.header {
  font-weight: 900;
  font-size: 1.5em;
}
.card-container {
  display: flex;
  flex-wrap: wrap;
  gap: 1em;
}

.container {
  margin-top: 2.5em;
  margin-bottom: 2.5em;
}
</style>
