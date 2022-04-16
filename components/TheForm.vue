<template>
  <form action="#" class="form">
    <label for="name" class="visually-hidden">Ваше имя</label>
    <input type="text" id="name" placeholder="Ваше имя" class="input">
    <label for="phone" class="visually-hidden">Номер телефона</label>
    <input type="tel" v-mask="'+7 (9##) ###-##-##'" v-model="phone" id="phone" placeholder="Номер телефона" class="input">
    <button type="submit" class="btn btn--primary">Заказать ремонт сейчас</button>
    <p class="form__description description description--secondary">
      Отправляя данную форму, вы соглашаетесь с
      <NuxtLink to="/privacy/" classs="description__link">
        политикой конфиденциальности
      </NuxtLink>
      и
      <NuxtLink to="/data/" class="description__link">
        политикой обработки данных
      </NuxtLink>
    </p>
  </form>
</template>

<script>
import Vue from 'vue';
import VueMask from 'v-mask';
Vue.use(VueMask)

export default {
  name: "TheForm",
  data () {
    return {
      phone: ''
    }
  }
}
</script>

<style lang="scss" scoped>
.form {
  display: flex;
  flex-direction: column;
  padding: 6.8% 5.2% 4.4%;
  background-color: #E2E2E2;
  border-radius: 7px;

  &__description {
    font-size: 0.91rem;
    text-align: center;
    margin-top: 12px;
  }

  &--secondary {
    background: none;
    padding: 0;
  }
}

.input {
  border-radius: 7px;
  color: #000;
  padding: 16px 30px;
  margin-bottom: 23px;
  box-shadow: 0px 0px 10px rgba(0, 0, 0, 0.25);
  font-size: 1rem;
  font-weight: 500;
  outline: none;
  border: 3px solid rgba(0, 0, 0, 0);
  transition: border-color 0.5s;

  &:focus {
    border-color: #5b93e2;
  }

  &::placeholder {
    color: #707070;
  }
}

</style>
