<template>
  <section class="section container" id="kind">
    <h2 class="heading heading--h2">Какую технику ремонтируем?</h2>
    <p class="description description--secondary">Мы ремонтируем любую бытовую технику в том числе и от самых известных компаний</p>
    <ul class="kind-gallery">
      <li class="kind-gallery__item">
        <img src="@/assets/images/lg.svg" alt="LG">
      </li>
      <li class="kind-gallery__item">
        <img src="@/assets/images/samsung.svg" alt="Samsung">
      </li>
      <li class="kind-gallery__item">
        <img src="@/assets/images/beko.svg" alt="Beko">
      </li>
      <li class="kind-gallery__item">
        <img src="@/assets/images/bosch.svg" alt="Bosch">
      </li>
    </ul>
  </section>
</template>

<script>
export default {
  name: "TechKind"
}
</script>

<style lang="scss" scoped>
.kind-gallery {
  display: flex;
  flex-wrap: nowrap;
  justify-content: space-between;
  align-items: center;

  &__item {
    @media (max-width: 768px) {
      width: 18%;
    }
  }
}

@import '~@/assets/scss/base/mixins';
@include section-settings(90px, 90px, 750px, 30px);
</style>
