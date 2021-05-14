<template>
  <div>
    <Card>
      <Filters v-for="filter in filters" :key="filter.id">
        <template #title>
          <h4>{{ filter.title }}</h4>
        </template>
        <template #content>
          <vs-radio
            v-for="(item, idx) in filter.items"
            :key="idx"
            v-model="option"
            val="1"
          >
            {{ item }}
          </vs-radio>
        </template>
      </Filters>
    </Card>
  </div>
</template>

<script>
export default {
  data: () => ({
    option: false,
    filters: [
      {
        id: 1,
        title: 'Multi Range',
        items: ['All', '<= $10', '$10 - $100', '$100 - $500', '>= $500'],
      },
      {
        id: 2,
        title: 'Categories',
        items: [
          'Appliances',
          'Audio',
          'Cameras & Camcorders',
          'Car Electronics & GPS',
          'Cell Phones',
          'Computers & Tablets',
          'Health, Fitness & Beauty',
          'Office & School Supplies',
          'TV & Home Theater',
          'Video Games',
        ],
      },
      {
        id: 3,
        title: 'Brands',
        items: [
          'Insignia™',
          'Samsung',
          'Metra',
          'HP',
          'Apple',
          'GE',
          'Sony',
          'Incipio',
          'KitchenAid',
          'Whirlpool',
        ],
      },
    ],
  }),
}
</script>

<style lang="scss" scoped></style>
