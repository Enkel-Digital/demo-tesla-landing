<template>
  <nav
    class="navbar hero-head is-marginless heading has-text-weight-bold is-white navbar-padding"
    role="navigation"
    aria-label="main navigation"
  >
    <div class="navbar-brand">
      <a class="navbar-item" href="https://www.tesla.com/" target="_blank">
        <img
          src="../assets/images/tesla.svg"
          alt="tesla logo"
          style="width: 6.25rem; height: 1rem"
        />
      </a>

      <a
        role="button"
        class="navbar-burger"
        :class="{ 'is-active': showMobileMenu }"
        aria-label="menu"
        aria-expanded="false"
        @click="showMobileMenu = !showMobileMenu"
      >
        <i
          class="fas fa-3x fa-bars has-text-black mt-4"
          style="width: 1rem; height: 1rem"
        />
      </a>
    </div>

    <div
      class="navbar-menu has-text-right"
      :class="{ 'is-active': showMobileMenu }"
    >
      <div class="navbar-end">
        <a class="navbar-item">SHOP</a>
        <a class="navbar-item">SIGN IN</a>
      </div>
    </div>
  </nav>
</template>

<script>
export default {
  name: "HeroHead",
  data() {
    return {
      showMobileMenu: false,
    };
  },
};
</script>

<style scoped>
/* navbar padding changes from desktop/tablet to mobile */
.navbar-padding {
  padding: 0 10%;
}
@media (max-width: 1024px) {
  .navbar-padding {
    padding: 0;
  }
}
</style>
