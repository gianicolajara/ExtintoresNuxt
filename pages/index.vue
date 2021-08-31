<template>
  <div>
    <div class="container">
      <Hero />
      <LargeCardDisplay
        v-for="largeCard in largeCardInfo"
        :key="largeCard.id"
        :card="largeCard"
      />
      <SmallCardDisplay
        v-for="smallCard in smallCardInfo"
        :key="smallCard.id"
        :card="smallCard"
      />
    </div>
  </div>
</template>

<script>
import Hero from '../components/Hero.vue'
import LargeCardDisplay from '../components/LargeCardDisplay.vue'
import SmallCardDisplay from '../components/SmallCardDisplay.vue'
import { largeCardSections, smallCardSections } from '@/assets/data.js'
export default {
  components: {
    Hero,
    LargeCardDisplay,
    SmallCardDisplay,
  },
  data() {
    return {
      largeCardInfo: largeCardSections,
      smallCardInfo: smallCardSections,
    }
  },
}
</script>

<style scoped>
.container {
  max-width: 850px;
}
</style>
