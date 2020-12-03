<template>
  <div>
    <vs-navbar
      v-model="active"
      color="#fff"
      square
      shadow-scroll
      center-collapsed
    >
      <template #left>
        <nuxt-link to="/" class="branding">
          <img src="karobaarlogo.svg" alt="" />
        </nuxt-link>
      </template>

      <template #right>
        <vs-navbar-item id="team" to="/team" :active="active == 'team'">
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
