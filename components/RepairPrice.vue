<template>
  <section class="section container col-2" id="price">
    <div class="text">
      <h2 class="heading heading--h2">Сколько будет стоить ремонт?</h2>
      <p class="description description--secondary">Невозможно оценить стоимость ремонта, не выслушав все ваши пожелания. Оставьте свой номер телефона для того, чтобы мы вам перезвонили и узнали о всех нюансах.</p>
    </div>
    <TheForm />
  </section>
</template>

<script>
import Vue from 'vue';
import VueMask from 'v-mask';
Vue.use(VueMask)

export default {
  name: "RepairPrice",
  data () {
    return {
      phone: ''
    }
  }
}
</script>

<style lang="scss" scoped>
@import '~@/assets/scss/base/mixins';
@include section-settings(82px, 74px, none, 25px);

.btn[type=submit] {
  background-color: #00327B;
  padding: 3% 5px;

  @media (max-width: 425px) {
    padding: 5% 5px;
  }
}

.description__link {
  display: inline-block;
  color: inherit !important;
  text-decoration: underline;
}
</style>
