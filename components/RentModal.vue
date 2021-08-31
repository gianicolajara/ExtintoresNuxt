<template>
  <div>
    <b-button id="show-btn" variant="danger w-100" @click="showModal"
      >Rent</b-button
    >

    <b-modal ref="my-modal" hide-footer title="Using Component Methods">
      <div class="calendar-container mb-3">
        <div class="text-container mb-3">
          Lorem ipsum dolor sit, amet consectetur adipisicing elit. Dolorem
          unde, suscipit vitae saepe magnam iusto officia voluptatem ipsam, enim
          aut recusandae sit impedit culpa distinctio eos exercitationem. Enim,
          aspernatur neque.
        </div>
        <vc-date-picker :value="null" color="red" is-dark is-range />
      </div>

      <b-button
        id="show-btn"
        variant="outline-danger w-100"
        @click="
          () => {
            addItem(product.id)
            hideModal()
          }
        "
        >Order</b-button
      >
    </b-modal>
  </div>
</template>

<script>
import { mapMutations } from 'vuex'
export default {
  props: {
    product: {
      type: Object,
      default: null,
    },
  },
  methods: {
    showModal() {
      this.$refs['my-modal'].show()
    },
    hideModal() {
      this.$refs['my-modal'].hide()
    },
    ...mapMutations(['addItem']),
  },
}
</script>

<style scoped>
.calendar-container {
  display: flex;
  flex-direction: row;
}
</style>
