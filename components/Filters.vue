<template>
  <div>
    <div class="title__wrapper">
      <slot name="title"></slot>
    </div>
    <div class="content__wrapper">
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
.title__wrapper {
  font-size: 18px;
  color: #393939;
}
.content__wrapper {
  font-size: 16px;
  padding: 0.8rem;
  line-height: 1.8;
  text-align: left;
  justify-content: flex-start;
}
</style>
