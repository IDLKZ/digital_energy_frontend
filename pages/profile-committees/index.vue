<template>
  <div class="container py-24 mx-auto md:px-6">
    <!-- Section: Design Block -->
    <section class="text-center">
      <h2 class="mb-12 text-3xl font-bold">
        Профильные комитеты<u class="text-primary dark:text-primary-400"></u>
      </h2>

      <div class="lg:gap-xl-12 grid gap-x-6 md:grid-cols-3 xl:grid-cols-4">
        <div v-for="item in teams.data" class="mb-6 lg:mb-3">
          <div
            class="block rounded-lg bg-white shadow-[0_2px_15px_-3px_rgba(0,0,0,0.07),0_10px_20px_-2px_rgba(0,0,0,0.04)] dark:bg-neutral-700">
            <div class="relative overflow-hidden bg-cover bg-no-repeat">
              <!--                <img src="https://mdbcdn.b-cdn.net/img/new/avatars/6.jpg" class="w-full rounded-t-lg" />-->
              <div class="bg-img" :style="{ 'background-image' : 'url('+getImageUrlFromBack(item.attributes.image.data.attributes.url)+')' }"></div>
              <NuxtLink :to="`/profile-committees/${item.id}`">
                <div class="absolute top-0 right-0 bottom-0 left-0 h-full w-full overflow-hidden bg-fixed"></div>
              </NuxtLink>
              <svg class="absolute text-white dark:text-neutral-700 left-0 bottom-0" xmlns="http://www.w3.org/2000/svg"
                   viewBox="0 0 1440 320">
                <path fill="currentColor"
                      d="M0,288L48,272C96,256,192,224,288,197.3C384,171,480,149,576,165.3C672,181,768,235,864,250.7C960,267,1056,245,1152,250.7C1248,256,1344,288,1392,304L1440,320L1440,320L1392,320C1344,320,1248,320,1152,320C1056,320,960,320,864,320C768,320,672,320,576,320C480,320,384,320,288,320C192,320,96,320,48,320L0,320Z">
                </path>
              </svg>
            </div>
            <div class="p-6">
              <h5 class="mb-4 text-lg font-bold">{{item.attributes.name}}</h5>
              <p class="mb-4 text-neutral-500 dark:text-neutral-300">{{item.attributes.position}}</p>
              <NuxtLink :to="`/profile-committees/${item.id}`" class="px-2">
                <!-- GitHub -->
                Подробнее
              </NuxtLink>
            </div>
          </div>
        </div>
      </div>
    </section>
    <!-- Section: Design Block -->

  </div>
</template>

<script>
import constants from "~/helpers/constants";
export default {
  name: "index",
  data() {
    return {

    }
  },
  async asyncData({ $axios }) {
    const teams = await $axios.$get(constants.baseApiUrl+'/profilnye-komiteties?populate=*')
    return { teams }
  },
  methods: {
    getImageUrl(url) {
      return require(`@/assets/images/profiles/${url}`)
    },
    getImageUrlFromBack(url) {
      return constants.baseUrl+url;
    }
  }
}
</script>

<style scoped>
.bg-img {
  background-size: cover!important;
  width: 100%;
  height: 400px;
  background-repeat: no-repeat!important;
  background-position: center!important;
}
</style>
