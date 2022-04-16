<template>
  <section class="section section--white container">
    <h2 class="heading heading--h2">Преимущества нашей работы</h2>

    <ol class="benefits">
      <li
        @click="showModal(benefit)"
        v-for="(benefit, index) in benefitsList"
        :key="index"
        class="benefits__item"
      >
        {{ benefit.name }}
      </li>
    </ol>

    <TheModal
      v-if="isActiveModal"
      :heading="modalHeading"
      @close-modal="isActiveModal = false"
    >
      <p class="description description--secondary">
        {{ modalContent }}
      </p>
    </TheModal>
  </section>
</template>

<script>
export default {
  name: "BenefitsOfWork",
  data () {
    return {
      modalHeading: '',
      modalContent: '',
      isActiveModal: false,
      benefitsList: [
        { name: 'Гарантия 1 месяц', content: 'Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat. Duis aute irure dolor in reprehenderit in voluptate velit esse cillum dolore eu fugiat nulla pariatur. Excepteur sint occaecat cupidatat non proident, sunt in culpa qui officia deserunt mollit anim id est laborum. Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat. Duis aute irure dolor in reprehenderit in voluptate velit esse cillum dolore eu fugiat nulla pariatur. Excepteur sint occaecat cupidatat non proident, sunt in culpa qui officia deserunt mollit anim id est laborum.' },
        { name: 'Экономно', content: 'Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat. Duis aute irure dolor in reprehenderit in voluptate velit esse cillum dolore eu fugiat nulla pariatur. Excepteur sint occaecat cupidatat non proident, sunt in culpa qui officia deserunt mollit anim id est laborum. Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat. Duis aute irure dolor in reprehenderit in voluptate velit esse cillum dolore eu fugiat nulla pariatur. Excepteur sint occaecat cupidatat non proident, sunt in culpa qui officia deserunt mollit anim id est laborum.' },
        { name: 'Примеры работ', content: 'Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat. Duis aute irure dolor in reprehenderit in voluptate velit esse cillum dolore eu fugiat nulla pariatur. Excepteur sint occaecat cupidatat non proident, sunt in culpa qui officia deserunt mollit anim id est laborum. Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat. Duis aute irure dolor in reprehenderit in voluptate velit esse cillum dolore eu fugiat nulla pariatur. Excepteur sint occaecat cupidatat non proident, sunt in culpa qui officia deserunt mollit anim id est laborum.' }
      ]
    }
  },
  methods: {
    showModal (benefit) {
      this.modalHeading = benefit.name
      this.modalContent = benefit.content
      this.isActiveModal = true
    }
  }
}
</script>

<style lang="scss" scoped>
.benefits {
  display: grid;
  grid-template-columns: repeat(3, 1fr);
  column-gap: 20%;

  &__item {
    background-color: #fff;
    color: #000;
    font-size: 1.5rem;
    font-weight: 600;
    padding: 6% 5px;
    border-radius: 9px;
    text-align: center;
    cursor: pointer;

    @media screen and (max-width: 1024px) {
      font-size: 1.1rem;
    }

    @media screen and (max-width: 425px) {
      font-size: 1rem;
    }
  }

  @media screen and (max-width: 1024px) {
    column-gap: 5%;
  }

  @media (max-width: 425px) {
    grid-template-columns: 1fr;
    row-gap: 5%;
    font-size: 1rem;
  }
}

.section {
  background-image: url('~@/assets/images/benefits.png');
}

@import '~@/assets/scss/base/mixins';
@include section-settings(82px, 107px, auto, 6%);
</style>
