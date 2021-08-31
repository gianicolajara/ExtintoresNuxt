<template>
  <div>
    <div class="container">
      <LargeCardDisplay
        v-for="cardInfo in largeCardInfo.slice(0, 1)"
        :key="cardInfo.id"
        :card="cardInfo"
      />
      <SmallCardDisplay
        v-for="cardInfo in smallCardInfo"
        :key="cardInfo.id"
        :card="cardInfo"
      />
    </div>
  </div>
</template>

<script>
import LargeCardDisplay from '../../components/LargeCardDisplay.vue'
import SmallCardDisplay from '../../components/SmallCardDisplay.vue'
import { largeCardSections, smallCardSections } from '@/assets/data.js'
export default {
  components: { LargeCardDisplay, SmallCardDisplay },
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
  width: 850px;
}
</style>
