<template>
  <div>
    <TheHeader />
    <FirstSection />
    <TechKind />
    <BenefitsOfWork />
    <RepairPrice />
    <TheFooter />
  </div>
</template>

<script>
export default {
  name: 'IndexPage',
  head: {
    title: 'Главная страница - ZA-Remont',
    meta: [
      { name: 'description', content: 'Здесь описание главной страницы!' }
    ]
  }
}
</script>

<style lang="scss">
.nav__link {
  @media (max-width: 768px) {
    color: #000 !important;
  }
}
</style>
