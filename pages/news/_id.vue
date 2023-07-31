<template>
  <div class="container py-24 mx-auto md:px-6">
    <!-- Section: Design Block -->
    <section>
      <img :src="getImageUrlFromBack(blog.data.attributes.images.data[0].attributes.url)"
           class="mb-6 w-full rounded-lg shadow-lg dark:shadow-black/20" alt="image" />

      <h1 class="mb-6 text-3xl font-bold">
        {{ blog.data.attributes.title }}
      </h1>

      <p>
        {{ blog.data.attributes.description }}
      </p>
    </section>
    <!-- Section: Design Block -->
  </div>
</template>

<script>
import constants from "~/helpers/constants";
  export default {
    async asyncData ({params, $axios}) {
      const blog = await $axios.$get(constants.baseApiUrl + '/blogs/' + params.id + '?populate=*')
      return { blog }
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
