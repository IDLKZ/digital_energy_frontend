<template>
  <div class="container py-24 mx-auto md:px-6">
    <!-- Section: Design Block -->
    <section class="text-center lg:text-left">
      <div class="py-12 md:px-6 md:px-12">
        <div class="container mx-auto xl:px-32">
          <div class="flex grid items-center lg:grid-cols-2">
            <div class="mb-12 md:mt-12 lg:mt-0 lg:mb-0">
              <div
                class="relative z-[1] block rounded-lg bg-[hsla(0,0%,100%,0.55)] px-6 py-12 shadow-[0_2px_15px_-3px_rgba(0,0,0,0.07),0_10px_20px_-2px_rgba(0,0,0,0.04)] backdrop-blur-[25px] dark:bg-[hsla(0,0%,5%,0.7)] dark:shadow-black/20 md:px-12 lg:-mr-14">
                <h2 class="mb-2 text-3xl font-bold text-primary dark:text-primary-400">
                  {{expert.data.attributes.name}}
                </h2>
                <p class="mb-4 font-semibold">{{expert.data.attributes.job}}</p>
                <p class="mb-6 text-neutral-500 dark:text-neutral-300">
                  <strong>Дата рождения: </strong> {{expert.data.attributes.birthday}}
                </p>
                <p class="mb-6 text-neutral-500 dark:text-neutral-300">
                  <strong>Контактные данные: </strong> {{expert.data.attributes.phone}} / {{expert.data.attributes.email}}
                </p>
                <p class="mb-6 text-neutral-500 dark:text-neutral-300">
                  <strong>Информация об образовании, квалификации, ученой степени: </strong> {{expert.data.attributes.education}}
                </p>
                <p class="mb-6 text-neutral-500 dark:text-neutral-300">
                  <strong>Информация о трудовой деятельности и текушее место работы: </strong> {{expert.data.attributes.works}}
                </p>
                <p class="mb-6 text-neutral-500 dark:text-neutral-300">
                  <strong>Участие в проектах (по желанию): </strong> {{expert.data.attributes.projects}}
                </p>

              </div>
            </div>
            <div class="md:mb-12 lg:mb-0">
              <img :src="getImageUrlFromBack(expert.data.attributes.image.data.attributes.url)"
                   class="lg:rotate-[6deg] w-full rounded-lg shadow-lg dark:shadow-black/20" alt="image" />
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
  async asyncData ({params, $axios}) {
    const expert = await $axios.$get(constants.baseApiUrl + '/eksperties/' + params.id + '?populate=*')
    return { expert }
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
