<template>
  <section class="py-5">
    <div class="container px-4 px-lg-5 my-5">
      <div class="row gx-4 gx-lg-5 align-items-center">
        <div class="col-md-6">
          <img
            class="card-img-top mb-5 mb-md-0"
            :src="$store.state.itemPreview.image"
            alt="..."
          />
        </div>
        <div class="col-md-6">
          <div class="small mb-1">{{ $store.state.itemPreview.id }}</div>
          <h1 class="display-5 fw-bolder">
            {{ $store.state.itemPreview.title }}
          </h1>
          <div class="fs-5 mb-5">
            <span>${{ $store.state.itemPreview.price }}</span>
          </div>
          <p class="lead">{{ $store.state.itemPreview.description }}</p>
          <div class="d-flex">
            <router-link
              to="/cart"
              class="btn btn-outline-dark flex-shrink-0"
              @click="$store.commit('addToCart', item)"
            >
              <i class="bi-cart-fill me-1"></i>
              Add to cart
            </router-link>
          </div>
        </div>
      </div>
    </div>
  </section>
</template>

<script>
export default {
  name: "ItemView",
  data() {
    return {
      item: {},
    };
  },
  async created() {
    const res = await fetch(
      `http://localhost:3000/products/${this.$store.state.itemPreview.id}`
    );
    this.item = await res.json();
  },
};
</script>

<style scoped>
.card-img-top {
  width: 600px;
  height: 700px;
}
</style>