<template>
 <nav class="nav">
   <button class="nav__btn btn" type="button" aria-expanded="false" aria-controls="menu" ref="navBtn" @click="showMenu">
     <img class="nav__btn-img" src="~@/assets/images/burger.svg" alt="Burger Menu">
   </button>
   <ul class="nav__list" id="menu" ref="navList">
     <li v-for="(link, index) in links" :key="index" class="nav__item" @click="hideMenu">
       <NuxtLink :to="link.href" class="nav__link">
         {{ link.text }}
       </NuxtLink>
     </li>
   </ul>
 </nav>
</template>

<script>
export default {
  name: "TheHeaderNav",
  data () {
    return {
      links: [
        { text: 'Услуги', href: '/#kind' },
        { text: 'О нас', href: '/about' },
        { text: 'Контакты', href: '/contacts' }
      ]
    }
  },
  methods: {
    showMenu (e) {
      const expanded = this.$refs.navBtn.getAttribute('aria-expanded') === 'true'
      this.$refs.navBtn.setAttribute('aria-expanded', !expanded)
      if (!expanded) {
        document.body.classList.add('fixed')
      } else {
        document.body.classList.remove('fixed')
      }
      this.$refs.navList.classList.toggle('active')
    },
    hideMenu () {
      document.body.classList.remove('fixed')
    }
  }
}
</script>

<style lang="scss" scoped>
.nav {
  &__btn {
    position: relative;
    background-color: #fff;
    box-shadow: 0px 0px 10px rgba(0, 0, 0, 0.25);
    width: 35px;
    height: 35px;
    padding: 5px;
    z-index: 3;

    @media (min-width: 769px) {
      display: none;
    }
  }

  &__list {
    display: flex;
    transition: top .5s;

    @media (max-width: 768px) {
      position: fixed;
      top: -100%;
      right: 0;
      left: 0;
      background-color: #fff;
      color: #000;
      height: 100vh;
      flex-direction: column;
      justify-content: center;
      align-items: center;
    }

    &.active {
      display: flex;
      top: 0;
    }
  }

  &__item {
    margin-right: 34px;
    font-size: 1.25rem;

    &:last-of-type {
      margin-right: 0;
    }

    @media (max-width: 768px) {
      margin-right: 0;
      width: 100%;
      text-align: center;
      font-size: 1.5rem;
      font-weight: 500;
      margin-bottom: 10px;
    }
  }

  &__link {
    text-decoration: none;
    color: inherit;

    @media (max-width: 768px) {
      display: block;
    }
  }
}
</style>
