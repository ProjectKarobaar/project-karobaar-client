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
        <img src="karobaarlogo.svg" class="branding" alt="" />
      </template>

      <template #right>
        <vs-navbar-item :active="active == 'team'" id="team">
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

<style lang="scss" scoped></style>
