<template>
  <div>
    <vs-navbar
      color="#fff"
      square
      shadowScroll
      center-collapsed
      v-model="active"
    >
      <template #left>
        <nuxt-link to="/" class="branding">
          <img src="karobaarlogo.svg" alt="" />
        </nuxt-link>
      </template>

      <template #right>
        <vs-navbar-item to="/team" :active="active == 'team'" id="team">
          team
        </vs-navbar-item>
      </template>
    </vs-navbar>
  </div>
</template>

<script>
export default {
  name: 'LandingNav',
  data: () => ({
    active: 'team',
  }),
}
</script>

<style lang="scss" scoped>
.team-link {
  color: #000;
}
.branding {
  width: 300px;
}
</style>
