<template>
  <div class="index-wrapper">
    <LandingPage />
  </div>
</template>

<script>
import LandingPage from '@/components/landing'

export default {
  layout: 'landinglayout',
  components: {
    LandingPage,
  },
}
</script>

<style lang="scss">
.index-wrapper {
  padding-top: 3rem;
}
</style>
