<template>
  <section class="section-links">
    <h2 class="visually-hidden">
      Ссылки на соц. сети
    </h2>

    <ul class="section-links__list">
      <li class="section-links__item phone-link">
        <a href="#" class="section-links__link">
          <img src="~@/assets/images/phone.svg" alt="Phone">
        </a>
      </li>
      <li class="section-links__item telegram-link">
        <a href="#" class="section-links__link">
          <img src="~@/assets/images/telegram.svg" alt="Telegram">
        </a>
      </li>
      <li class="section-links__item whatsapp-link">
        <a href="#" class="section-links__link">
          <img src="~@/assets/images/whatsapp.svg" alt="Whatsapp">
        </a>
      </li>
    </ul>
  </section>
</template>

<script>
export default {
  name: "LinksSection"
}
</script>

<style lang="scss" scoped>
.section-links {
  &__list {
    display: grid;
    grid-template-columns: repeat(3, 1fr);
    column-gap: 30px;
    margin-top: 50px;
    margin-bottom: 74px;

    @media (max-width: 768px) {
      grid-template-columns: 1fr;
      row-gap: 2%;
    }
  }

  &__item {
    display: grid;
    border-radius: 31px;
  }

  &__link {
    text-align: center;
    padding: 28% 0;

    @media (max-width: 768px) {
      padding: 5% 0;
    }
  }
}

.phone-link {
  background-color: #0447A9;
}

.telegram-link {
  background-color: #0088CC;
}

.whatsapp-link {
  background-color: #25D366;
}
</style>
