<template>
  <div class="container py-24 mx-auto md:px-6">
    <!-- Section: Design Block -->
    <section class="text-center">
      <h2 class="mb-12 text-3xl font-bold">
        Эксперты <u class="text-primary dark:text-primary-400"></u>
      </h2>

      <div class="lg:gap-xl-12 grid gap-x-6 md:grid-cols-3 xl:grid-cols-4">
        <div v-for="item in experts.data" class="mb-12">
          <img :src="getImageUrlFromBack(item.attributes.image.data.attributes.url)"
               class="mx-auto mb-4 rounded-full shadow-lg dark:shadow-black/20" alt="" style="max-width: 100px" />

          <NuxtLink :to="`/experts/${item.id}`"><p class="mb-2 font-bold">{{item.attributes.name}}</p></NuxtLink>
        </div>
      </div>
    </section>
    <!-- Section: Design Block -->
  </div>
</template>

<script>
import constants from "~/helpers/constants";

export default {
  name: "experts",
  async asyncData ({$axios}) {
    const experts = await $axios.$get(constants.baseApiUrl + '/eksperties?populate=*')
    return { experts }
  },
  methods: {
    getImageUrlFromBack(url) {
      return constants.baseUrl+url;
    }
  }
}
</script>

<style scoped>

</style>
