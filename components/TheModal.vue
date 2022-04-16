<template>
  <section class="modal">
    <div
      @click="$emit('close-modal')"
      class="modal__bg"
    >
    </div>

    <div class="modal__content">
      <div class="modal__header">
        <h2 class="heading heading--h2">
          {{ heading }}
        </h2>
        <img
          @click="$emit('close-modal')"
          class="btn"
          src="@/assets/images/close.svg"
          alt="ico">
      </div>
      <slot></slot>
    </div>
  </section>
</template>

<script>
export default {
  name: "TheModal",
  props: {
    heading: {
      type: String,
      required: true
    }
  }
}
</script>

<style lang="scss" scoped>
.modal {
  position: fixed;
  top: 0;
  right: 0;
  bottom: 0;
  left: 0;
  color: #000;
  z-index: 4;
  transition: opacity .5s;

  &__bg {
    position: absolute;
    top: 0;
    right: 0;
    bottom: 0;
    left: 0;
    background-color: rgba(0, 0, 0, 0.5);
  }

  &__content {
    position: absolute;
    top: 50%;
    right: 50%;
    background-color: #fff;
    width: 650px;
    padding: 2%;
    border-radius: 7px;
    transform: translate(50%, -50%);
    z-index: 2;

    @media (max-width: 425px) {
      top: 0;
      right: 0;
      bottom: 0;
      left: 0;
      max-width: 100%;
      border-radius: 0;
      transform: none;
      padding: 4%;
    }
  }

  &__header {
    display: flex;
    justify-content: space-between;
    align-items: center;
    margin-bottom: 3%;
  }

  &__form {
    position: absolute;
    top: 50%;
    left: 50%;
    transform: translate(-50%, -50%);
    width: 92%;
  }
}
</style>
