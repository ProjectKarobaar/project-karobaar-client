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
@media only screen and (min-width: 600px) {
  .index-wrapper {
    padding-top: 1.2rem;
  }
}
</style>
