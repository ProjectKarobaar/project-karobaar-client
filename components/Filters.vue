<template>
  <div class="filter__wrapper">
    <template v-if="filter.type === `radio`">
      <div class="title__wrapper">
        <h4>{{ filter.title }}</h4>
      </div>
      <div class="content__wrapper">
        <vs-radio
          v-for="(item, idx) in filter.items"
          :key="idx"
          v-model="option"
          val="1"
        >
          {{ item }}
        </vs-radio>
      </div>
    </template>
    <template v-if="filter.type === `rangeslider`">
      <div class="title__wrapper">
        <h4>{{ filter.title }}</h4>
      </div>
      <div class="content__wrapper">
        <MultiRangeSlider />
      </div>
    </template>
  </div>
</template>

<script>
export default {
  props: {
    filter: {
      type: Object,
      default: () => {},
    },
  },
  data: () => ({
    option: false,
  }),
}
</script>

<style lang="scss" scoped>
.filter__wrapper {
  margin-bottom: 1rem;
}

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
