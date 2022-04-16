<template>
  <div>
    <TheHeader />
    <AboutUs />
  </div>
</template>

<script>
export default {
  name: "about",
  head: {
    title: 'О нас - ZA-Remont',
    meta: [
      { name: 'description', content: 'Здесь страницы "О нас"!' }
    ]
  }
}
</script>

<style lang="scss" scoped>
.header {
  color: #000 !important;
}
</style>
