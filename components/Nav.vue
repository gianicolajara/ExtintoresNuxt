<template>
  <header>
    <b-navbar toggleable="lg" type="dark" variant="dark">
      <b-navbar-brand>
        <NuxtLink to="/" class="text-white text-decoration-none">
          Gianicola
        </NuxtLink>
      </b-navbar-brand>

      <b-navbar-toggle target="nav-collapse"></b-navbar-toggle>

      <b-collapse id="nav-collapse" is-nav>
        <b-navbar-nav>
          <b-nav-item>
            <NuxtLink to="/products" class="text-white text-decoration-none">
              Products
            </NuxtLink>
          </b-nav-item>
          <b-nav-item>
            <NuxtLink to="/my-items" class="text-white text-decoration-none">
              My Items
            </NuxtLink>
          </b-nav-item>
        </b-navbar-nav>
      </b-collapse>
    </b-navbar>
  </header>
</template>

<script>
export default {}
</script>

<style scoped></style>
