<template>
  <div>
    <MyItem v-for="item in myRentals" :key="item.id" :item="item" />
  </div>
</template>

<script>
import { mapState } from 'vuex'
import MyItem from '../components/MyItem.vue'
export default {
  components: { MyItem },
  layout: 'no-nav',
  computed: {
    ...mapState(['myRentals']),
  },
}
</script>

<style lang="scss" scoped></style>
