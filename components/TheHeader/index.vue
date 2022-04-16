<template>
  <header class="header container">
    <a href="/" class="header__logo">
      <img src="@/assets/images/logo.svg" alt="Logo">
    </a>

    <TheHeaderNav />

    <a href="tel:+79000000000" class="header__phone btn btn--primary">+7 (900) 000-00-00</a>
  </header>
</template>

<script>
export default {
  name: "TheHeader",
  props: ['isBlack']
}
</script>

<style lang="scss" scoped>
.header {
  display: flex;
  justify-content: space-between;
  align-items: center;
  position: absolute;
  top: 0;
  padding-top: 24px;
  padding-bottom: 24px;
  color: #fff;

  &__phone {
    @media (max-width: 768px) {
      display: none;
    }
  }
}
</style>
