<template>
  <div class="card">
    <div>
      <slot name="content"></slot>
    </div>
    <div>
      <slot name="footer"></slot>
    </div>
  </div>
</template>

<script>
export default {}
</script>

<style lang="scss" scoped>
.card {
  box-shadow: 0px 0px 20px 5px #e4e4e4;
  margin: 5rem;
  border-radius: 12px;
  width: fit-content;
  padding: 1.25rem;
}
</style>
