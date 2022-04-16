<template>
  <div>
    <TheHeader />
    <section class="section container">
      <h1 class="heading heading--h1">Контакты</h1>

      <section class="section-form">
        <h2 class="heading heading--h2">Свяжитесь с нами!</h2>

        <div class="col-2">
          <TheForm class="form--secondary" />

          <p class="col-2__desc description description--secondary">
            Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat.
          </p>
        </div>
      </section>

      <LinksSection />
    </section>
    <TheFooter />
  </div>
</template>

<script>
export default {
  name: "contacts",
  head: {
    title: 'Контакты - ZA-Remont',
    meta: [
      { name: 'description', content: 'Здесь описание контактов!' }
    ]
  }
}
</script>

<style lang="scss" scoped>
.col-2 {
  margin-top: 3%;

  &__desc {
    font-size: 1.5rem;
    color: #676767;
    line-height: 2rem;

    @media (max-width: 768px) {
      display: none;
    }
  }
}

.header {
  color: #000 !important;
}

.section.container {
  margin-top: 144px;

  @media (max-width: 768px) {
    margin-top: 11%;
  }

  @media (max-width: 425px) {
    margin-top: 20%;
  }
}

.heading.heading--h1 {
  margin-bottom: 4%;
}

.section-form {
  background-color: #EAEAEA;
  border-radius: 22px;
  padding: 4% 5%;

  @media (max-width: 425px) {
    padding: 6% 5%;
    border-radius: 10px;
  }
}
</style>
