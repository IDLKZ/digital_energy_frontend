<template>
  <!-- Container for demo purpose -->
  <div class="container py-24 mx-auto md:px-6">
    <!-- Section: Design Block -->
    <section class="mb-32 text-center">
      <h2 class="mb-12 text-center text-3xl font-bold">Последние новости</h2>

      <div class="grid gap-6 lg:grid-cols-3 xl:gap-x-12">

        <div v-for="blog in blogs.data" class="mb-6 lg:mb-0">
          <div class="relative mb-6 overflow-hidden rounded-lg bg-cover bg-no-repeat shadow-lg dark:shadow-black/20"
               data-te-ripple-init data-te-ripple-color="light">
<!--            <img :src="getImageUrlFromBack(blog.attributes.images.data[0].attributes.url)" class="w-full" alt="Louvre" />-->
            <div :style="{ 'background-image' : 'url('+ getImageUrlFromBack(blog.attributes.images.data[0].attributes.url)+')' }" class="w-full bg-img" alt="Louvre" />
            <NuxtLink :to="`/news/${blog.id}`">
              <div
                class="absolute top-0 right-0 bottom-0 left-0 h-full w-full overflow-hidden bg-fixed opacity-0 transition duration-300 ease-in-out hover:opacity-100 bg-[hsla(0,0%,98.4%,.15)]">
              </div>
            </NuxtLink>
          </div>
          <NuxtLink :to="`/news/${blog.id}`">
          <h5 class="mb-3 text-lg font-bold text-black">{{blog.attributes.title}}</h5>
          </NuxtLink>
          <div class="mb-3 flex items-center justify-center text-sm font-medium text-danger dark:text-danger-500">
            <svg xmlns="http://www.w3.org/2000/svg" fill="none" viewBox="0 0 24 24" stroke-width="2"
                 stroke="currentColor" class="mr-2 h-5 w-5">
              <path stroke-linecap="round" stroke-linejoin="round"
                    d="M12.75 3.03v.568c0 .334.148.65.405.864l1.068.89c.442.369.535 1.01.216 1.49l-.51.766a2.25 2.25 0 01-1.161.886l-.143.048a1.107 1.107 0 00-.57 1.664c.369.555.169 1.307-.427 1.605L9 13.125l.423 1.059a.956.956 0 01-1.652.928l-.679-.906a1.125 1.125 0 00-1.906.172L4.5 15.75l-.612.153M12.75 3.031a9 9 0 00-8.862 12.872M12.75 3.031a9 9 0 016.69 14.036m0 0l-.177-.529A2.25 2.25 0 0017.128 15H16.5l-.324-.324a1.453 1.453 0 00-2.328.377l-.036.073a1.586 1.586 0 01-.982.816l-.99.282c-.55.157-.894.702-.8 1.267l.073.438c.08.474.49.821.97.821.846 0 1.598.542 1.865 1.345l.215.643m5.276-3.67a9.012 9.012 0 01-5.276 3.67m0 0a9 9 0 01-10.275-4.835M15.75 9c0 .896-.393 1.7-1.016 2.25" />
            </svg>
          </div>
        </div>

      </div>
      <div>
        <Paginate
          :page-count="this.blogs.meta.pagination.pageCount"
          :click-handler="callBack"
          :prev-text="'Пред'"
          :next-text="'След'"
          :container-class="'list-style-none flex'"
          :page-class="'mx-3'"
          :page-link-class="'relative block rounded-full bg-transparent px-3 py-1.5 text-sm text-neutral-600 transition-all duration-300 hover:bg-neutral-100  dark:text-white dark:hover:bg-neutral-700 dark:hover:text-white'">
        </Paginate>
      </div>
    </section>
    <!-- Section: Design Block -->
  </div>
</template>

<script>
import constants from "~/helpers/constants";
import Paginate from "vuejs-paginate";
export default {
  name: "index",
  components: {
    Paginate
  },
  data() {
    return {
      blogs: []
    }
  },
  async asyncData({$axios}) {
    const blogs = await $axios.$get(constants.baseApiUrl+'/blogs?populate=*&pagination[page]=1&pagination[pageSize]=10')
    return { blogs }
  },
  methods: {
    async getItems() {
      await this.$axios.$get(constants.baseApiUrl+'/blogs?populate=*&pagination[page]=1&pagination[pageSize]=10')
        .then(res => {
          this.blogs = res
        })
    },
    getImageUrlFromBack(url) {
      return constants.baseUrl+url;
    },
    async callBack(pageNum) {
      await this.$axios.$get(constants.baseApiUrl+`/blogs?populate=*&pagination[page]=${pageNum}&pagination[pageSize]=1`)
        .then(res => {
          this.blogs = res
        })
    }
  },
  created() {
    this.getItems()
  }
}
</script>

<style scoped>
  .bg-img {
    background-size: cover!important;
    width: 100%;
    height: 320px;
    background-repeat: no-repeat!important;
    background-position: center!important;
  }
</style>
