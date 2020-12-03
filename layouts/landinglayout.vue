<template>
  <div class="main">
    <LandingNav class="navbar" />

    <Nuxt />
  </div>
</template>
<script>
import LandingNav from '@/components/LandingNav'
export default {
  components: {
    LandingNav,
  },
}
</script>
<style lang="scss">
.navbar {
  margin-bottom: 44px;
}
</style>
