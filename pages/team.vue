<template>
  <div class="team-wrapper">
    <Team />
  </div>
</template>

<script>
import Team from '@/components/Team'
export default {
  layout: 'landinglayout',
  components: {
    Team,
  },
}
</script>

<style lang="scss" scoped>
.team-wrapper {
  padding: 1.5rem 0;
}
</style>
