<template>
  <div class="basic-layout">
    <Menu />
    <div class="ui container">
      <slot />
    </div>
  </div>

  <Cart />
</template>

<script>
import Menu from '../components/Menu.vue';
import Cart from '../components/Cart/Cart.vue';

export default {
  name: 'BasicLayouts',
  components: {
    Menu,
    Cart,
  },
};
</script>

<style>
.basic-layout{
  background-color: rgb(41, 40, 40);
  background-image: "../assets/banner.png";
  backface-visibility: visible;
}
</style>
