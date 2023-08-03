<template>
<!--  <section class="fixed w-full z-20" :style="{ 'background': !view.topOfPage ? '#0C3759' : 'transparent'}">-->
  <section class="fixed w-full z-20" style="background: #0C3759">
  <div class="container-full navbar bg-transparent">
    <div class="container mx-auto">
    <div class="navbar justify-between">
      <div class="">
        <div class="dropdown">
          <label tabindex="0" class="btn btn-ghost lg:hidden">
            <svg xmlns="http://www.w3.org/2000/svg" class="h-5 w-5 text-white" fill="none" viewBox="0 0 24 24" stroke="currentColor"><path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M4 6h16M4 12h8m-8 6h16" /></svg>
          </label>
          <ul tabindex="0" class="menu menu-sm dropdown-content mt-3 z-[1] p-2 shadow bg-base-100 rounded-box w-52">
            <li><NuxtLink to="/news" class="text-white text-md">Новости</NuxtLink></li>
            <li><NuxtLink to="/about-us" class="text-white text-md">О Нас</NuxtLink></li>
            <li><NuxtLink to="/teams" class="text-white text-md">Наша команда</NuxtLink></li>
            <li><NuxtLink to="/associations" class="text-white text-md">Члены ассоциации</NuxtLink></li>
            <li><NuxtLink to="/about-consortium" class="text-white text-md">О консорциуме</NuxtLink></li>
            <li><NuxtLink to="/profile-committees" class="text-white text-md">Профильные комитеты</NuxtLink></li>
            <li><NuxtLink to="/experts" class="text-white text-md">Эксперты</NuxtLink></li>
          </ul>
        </div>
        <NuxtLink to="/"><img src="~/assets/images/nav_logo.png" class="w-full md:w-full"></NuxtLink>
      </div>
      <div class="">
        <div class="hidden lg:flex">
        <ul class="menu menu-horizontal px-1">
          <li><NuxtLink to="/news" class="text-white text-md">Новости</NuxtLink></li>
          <li><NuxtLink to="/about-us" class="text-white text-md">О Нас</NuxtLink></li>
          <li><NuxtLink to="/teams" class="text-white text-md">Наша команда</NuxtLink></li>
          <li><NuxtLink to="/associations" class="text-white text-md">Члены ассоциации</NuxtLink></li>
          <li class="dr-id relative">
            <a class="text-white text-md">Индустрия 4.0</a>
            <ul class="dr-content">
              <li><NuxtLink to="/about-consortium" class="text-white text-md">О консорциуме</NuxtLink></li>
              <li><NuxtLink to="/profile-committees" class="text-white text-md">Профильные комитеты </NuxtLink></li>
              <li><NuxtLink to="/experts" class="text-white text-md">Эксперты </NuxtLink></li>
            </ul>
          </li>
          <li><NuxtLink to="/contact" class="text-white text-md">Контакты</NuxtLink></li>
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

  .dr-content {
    display: none;
    position: absolute;
    top: 36px;
    left: 0;
    background: #0C3759
  }
  .dr-id:hover .dr-content {
    display: block;
  }
</style>
