<template>
  <footer class="footer container">
    <a href="/" class="footer__logo">
      <img src="@/assets/images/logo.svg" alt="Logo">
    </a>

    <nav class="footer__nav">
      <ul class="footer__nav-list">
        <li class="footer__nav-item">
          <NuxtLink to="/privacy" class="footer__nav-link">
            Политика конфиденциальности
          </NuxtLink>
        </li>
        <li class="footer__nav-item">
          <NuxtLink to="/data" class="footer__nav-link">
            Политика обработки данных
          </NuxtLink>
        </li>
      </ul>
    </nav>

    <a href="tel:+79000000000" class="footer__phone btn btn--primary">+7 (900) 000-00-00</a>
  </footer>
</template>

<script>
export default {
  name: "TheFooter"
}
</script>

<style lang="scss" scoped>
.footer {
  display: flex;
  justify-content: space-between;
  align-items: center;
  background-color: #000;
  padding-top: 20px;
  padding-bottom: 20px;
}

.footer__nav {
  &-list {
    display: flex;
  }

  &-item {
    margin-right: 30px;

    &:last-of-type {
      margin-right: 0;
    }

    @media (max-width: 768px) {
      display: none;
    }
  }

  &-link {
    text-decoration: none;
    color: #fff;
  }
}
</style>
