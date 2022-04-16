<template>
  <div>
    <section class="section section--white container">
      <div class="section__content">
        <h1 class="heading heading--h1">Ремонтируем бытовую технику любой сложности</h1>
        <p class="description">Мы починим вашу технику быстро и качественно, а также расскажем, как избежать поломок.</p>
        <button @click="isActiveModal = true" class="btn btn--primary">Заказать ремонт сейчас!</button>
      </div>
    </section>

    <TheModal
      heading="Закажите ремонт сейчас!"
      @close-modal="isActiveModal = false"
      v-if="isActiveModal"
    >
      <TheForm class="form--secondary modal__form" />
    </TheModal>
  </div>
</template>

<script>
export default {
  name: "FirstSection",
  data () {
    return {
      isActiveModal: false
    }
  }
}
</script>

<style lang="scss" scoped>
.section {
  background-image: url('~@/assets/images/bg.png');
}

@import '~@/assets/scss/base/mixins';
@include section-settings(220px, 183px, 586px, 25px);
</style>
