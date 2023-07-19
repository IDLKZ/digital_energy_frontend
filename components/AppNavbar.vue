<template>
  <section class="fixed w-full z-20" :style="{ 'background': !view.topOfPage ? '#0C3759' : 'transparent'}">
  <div class="container-full navbar bg-transparent">
    <div class="container mx-auto">
    <div class="navbar">
      <div class="navbar-start">
        <div class="dropdown">
          <label tabindex="0" class="btn btn-ghost lg:hidden">
            <svg xmlns="http://www.w3.org/2000/svg" class="h-5 w-5 text-white" fill="none" viewBox="0 0 24 24" stroke="currentColor"><path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M4 6h16M4 12h8m-8 6h16" /></svg>
          </label>
          <ul tabindex="0" class="menu menu-sm dropdown-content mt-3 z-[1] p-2 shadow bg-base-100 rounded-box w-52">
            <li><a class="text-black text-md">Новости</a></li>
            <li><a class="text-black text-md">О Нас</a></li>
            <li><a class="text-black text-md">Наша команда</a></li>
            <li><a class="text-black text-md">Проекты</a></li>
            <li><a class="text-black text-md">Иницитивы</a></li>
            <li><a class="text-black text-md">Эксперты</a></li>
          </ul>
        </div>
        <a href=""><img src="~/assets/images/nav_logo.png" class="w-full md:w-full"></a>
      </div>
      <div class="navbar-end">
        <div class="hidden lg:flex">
        <ul class="menu menu-horizontal px-1">
          <li><a class="text-white text-md">Новости</a></li>
          <li><a class="text-white text-md">О Нас</a></li>
          <li><a class="text-white text-md">Наша команда</a></li>
          <li><a class="text-white text-md">Проекты</a></li>
          <li><a class="text-white text-md">Иницитивы</a></li>
          <li><a class="text-white text-md">Эксперты</a></li>
        </ul>
        </div>
        <a class="btn text-white bg-transparent border border-white">Войти</a>
      </div>
    </div>
    </div>
  </div>
  </section>
</template>

<script>
export default {
  name: "AppNavbar",
  data () {
    return {
      view: {
        topOfPage: true
      }
    }
  },
  beforeMount() {
    window.addEventListener('scroll', this.handleScroll)
  },
  methods: {
    handleScroll(){
      if(window.pageYOffset>0){
        if(this.view.topOfPage) this.view.topOfPage = false
      } else {
        if(!this.view.topOfPage) this.view.topOfPage = true
      }
    }
  },
}
</script>

<style scoped>

</style>
