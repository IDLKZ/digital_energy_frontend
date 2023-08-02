<template>
  <section>
    <AppNavbarFront></AppNavbarFront>
    <Nuxt />
    <AppFooter></AppFooter>
  </section>

</template>

<script>
import "tw-elements/dist/css/tw-elements.min.css";
import AppNavbarFront from "../components/AppNavbarFront";
export default {
  name: "front",
  components: {AppNavbarFront}
}
</script>

<style scoped>

</style>
