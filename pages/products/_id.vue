<template>
  <div>
    <div v-if="product" class="container">
      <div class="show-item mt-5">
        <div class="show-item__img-container">
          <img
            :src="require(`@/assets/images/${product.image}`)"
            alt=""
            class="show-item__image"
          />
        </div>
        <div class="show-item__description-container">
          <h3 class="description__title">{{ product.title }}</h3>
          <p class="description__snnipet">{{ product.snippet }}</p>
          <RentModal :product="product" />
        </div>
      </div>
      <div class="show-warranty mt-5 mb-5">
        <div class="show-warranty__item">
          <h4 class="show-warranty__title">Super Effective</h4>
          <p class="show-warranty__body text-secondary">
            Lorem ipsum dolor sit amet consectetur adipisicing elit.
            Repudiandae, fuga nisi.
          </p>
        </div>
        <div class="show-warranty__item">
          <h4 class="show-warranty__title">Clean & Tidy</h4>
          <p class="show-warranty__body text-secondary">
            Lorem ipsum dolor sit amet consectetur adipisicing elit.
            Repudiandae, fuga nisi.
          </p>
        </div>
        <div class="show-warranty__item">
          <h4 class="show-warranty__title">Cancel Anytime</h4>
          <p class="show-warranty__body text-secondary">
            Lorem ipsum dolor sit amet consectetur adipisicing elit.
            Repudiandae, fuga nisi.
          </p>
        </div>
        <div class="show-warranty__item">
          <h4 class="show-warranty__title">Satisfaction</h4>
          <p class="show-warranty__body text-secondary">
            Lorem ipsum dolor sit amet consectetur adipisicing elit.
            Repudiandae, fuga nisi.
          </p>
        </div>
      </div>
      <div class="other-information">
        <hr />
        <p class="text-secondary">
          Lorem ipsum dolor sit amet consectetur adipisicing elit. Eos, quaerat
          asperiores repellendus ex qui et hic perferendis ducimus autem saepe
          exercitationem id incidunt aliquam quia assumenda eligendi doloremque
          quod quis?
        </p>
        <hr />
      </div>
      <Reviews />
    </div>
    <div v-else class="container">
      <PageNotFound />
    </div>
  </div>
</template>

<script>
import PageNotFound from '../../components/PageNotFound.vue'
import RentModal from '../../components/RentModal.vue'
import Reviews from '../../components/Reviews.vue'
export default {
  components: {
    PageNotFound,
    Reviews,
    RentModal,
  },
  computed: {
    product() {
      return this.$store.getters.getProductById(this.$route.params.id)
    },
  },
}
</script>

<style scoped>
.container {
  width: 850px;
}

.show-item {
  display: flex;
  width: 100%;
  height: 20em;
  gap: 2em;
  overflow: hidden;
}

.show-item__img-container {
  width: 60%;
}

.show-item__description-container {
  width: 40%;
}

.show-item__image {
  width: 100%;
  height: 100%;
  object-fit: cover;
  object-position: center;
}

.show-warranty__title {
  font-size: 1.2rem;
  font-weight: 700;
}
</style>
