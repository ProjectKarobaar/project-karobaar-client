<template>
  <div class="display__grid">
    <FilterBar class="sidebar" />
    <div class="cards"><ItemCard v-for="n in 6" :key="n" /></div>
  </div>
</template>

<script>
export default {}
</script>

<style lang="scss" scoped>
.display__grid {
  display: grid;
  padding: 3rem;
  gap: 32px;
  grid-template-rows: auto;
  grid-template-columns: 20% 80%;
  grid-template-areas: 'sidebar cards';

  .sidebar {
    grid-area: sidebar;
  }
  .cards {
    grid-area: cards;
    display: grid;
    gap: 32px;
    width: 100%;
    height: fit-content;
    place-items: center;
    grid-template-columns: repeat(3, 320px);
  }
}
</style>
