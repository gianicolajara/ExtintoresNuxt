<template>
  <div>
    <h3 class="mb-5">Customer Reviews</h3>
    <div v-if="!$fetchState.pending">
      <ReviewCard
        v-for="(person, index) in reviewers.results"
        :key="index"
        :person="person"
      />
    </div>
    <div v-else>loading...</div>
  </div>
</template>

<script>
export default {
  data() {
    return {
      reviewers: [],
    }
  },
  async fetch() {
    try {
      const res = await fetch('https://randomuser.me/api/?results=5')
      this.reviewers = await res.json()
    } catch (error) {
      // eslint-disable-next-line no-console
      console.log(error)
    }
  },
}
</script>

<style lang="scss" scoped></style>
