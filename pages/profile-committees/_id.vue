<template>
  <div class="container py-24 mx-auto md:px-6">
    <!-- Section: Design Block -->
    <section class="text-center md:text-left">
      <div class="block rounded-lg bg-white shadow-[0_2px_15px_-3px_rgba(0,0,0,0.07),0_10px_20px_-2px_rgba(0,0,0,0.04)] dark:bg-neutral-700">
        <div class="flex flex-wrap items-center">
          <div
            class="block w-full shrink-0 grow-0 basis-auto md:w-4/12 lg:flex">
            <img
              :src="getImageUrlFromBack(user.data.attributes.image.data.attributes.url)"
              alt="Trendy Pants and Shoes"
              class="w-full rounded-t-lg md:rounded-tr-none md:rounded-bl-lg" />
          </div>
          <div class="w-full shrink-0 grow-0 basis-auto md:w-8/12">
            <div class="px-6 py-12 md:px-12">
              <h2 class="mb-6 text-3xl font-bold">
                <span class="text-danger dark:text-danger-500">{{user.data.attributes.name}}</span>
              </h2>
              <p class="mb-6 pb-2">({{user.data.attributes.position}})</p>
              <p class="mb-6 pb-2 text-neutral-500 dark:text-neutral-300">
                {{user.data.attributes.description}}
              </p>
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
      const user = await $axios.$get(constants.baseApiUrl+`/api/profilnye-komiteties/${params.id}?populate=*`)
      return { user }
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
