<template>
  <div>
    <Card>
      <template #content>
        <div class="content__wrapper">
          <div class="img__wrapper">
            <img src="/item.png" alt="" />
          </div>
          <div class="price__wrapper">
            <h2><b> Item Name </b></h2>
            <h3><b> $399.00 </b></h3>
          </div>
          <div class="subtext__wrapper">
            <h4>Lorem ipsum dolor sit.</h4>
          </div>
        </div>
      </template>
      <template #footer>
        <div class="actionBtn__wrapper">
          <div class="wishlist">
            <vs-button
              danger
              border
              size="large"
              :active="active == 1"
              @click="active = 1"
            >
              <img
                :src="
                  active == 1
                    ? `/icons/heart-fill.svg`
                    : `/icons/heart-outline.svg`
                "
              />
              Wishlist
            </vs-button>
          </div>
          <div class="cart">
            <vs-button
              border
              size="large"
              :active="active == 2"
              @click="active = 2"
            >
              <img
                :src="
                  active == 2
                    ? `/icons/cart-fill.svg`
                    : `/icons/cart-outline.svg`
                "
              />
              {{ active == 2 ? 'View in cart' : 'Add to cart' }}
            </vs-button>
          </div>
        </div>
      </template>
    </Card>
  </div>
</template>

<script>
export default {
  data: () => ({
    active: 0,
  }),
}
</script>

<style lang="scss" scoped>
.content__wrapper {
  display: flex;
  align-items: center;
  flex-direction: column;
  margin-bottom: 1.5rem;
}
.img__wrapper {
  width: 200px;
  height: 200px;
  display: grid;
  place-items: center;

  img {
    width: 100%;
    height: 100%;
    padding: 1.2rem;
  }
}
.price__wrapper,
.actionBtn__wrapper {
  display: flex;
  width: 100%;
  justify-content: space-between;
}
.subtext__wrapper {
  width: 100%;
  justify-content: flex-start;
  color: rgb(50, 50, 50);
  font-weight: 200;
}
</style>
