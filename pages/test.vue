<template>
  <div>
    <Card>
      <template #content>
        <Filters v-for="(filter, idx) in filters" :key="idx" :filter="filter" />
      </template>
    </Card>
  </div>
</template>

<script>
export default {
  data: () => ({
    filters: [
      {
        id: 1,
        type: 'radio',
        title: 'Multi Range',
        items: ['All', '<= $10', '$10 - $100', '$100 - $500', '>= $500'],
      },
      {
        id: 2,
        title: 'Price Range',
        type: 'rangeslider',
      },
      {
        id: 3,
        type: 'radio',
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
        id: 4,
        type: 'radio',
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
