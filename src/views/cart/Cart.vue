<template>
  <div id="cart">
    <!-- 导航 -->
      <nav-bar class="nav-bar"><div slot="center">购物车({{cartCount}})</div></nav-bar>
    <!-- 商品列表 -->

    <!-- 底部汇总 -->
    <bottom-bar></bottom-bar>
  </div>
</template>

<script>
    import NavBar from 'components/common/navbar/NavBar'
    // import CartList from './childComps/CartList'
    import BottomBar from './childComps/BottomBar'

export default {
  name: 'Cart',
  components:{
      NavBar,
    //   CartList,
      BottomBar
  },
  
  computed:{
      // cartList() {
		  //   return this.$store.getters.cartList
      // },
      cartCount() {
		    return this.$store.getters.cartCount
      }
    },
 
};
</script>

<style scoped>
    #cart {
    /*position: relative;*/
    height: 100vh;
  }

  .nav-bar {
    background-color: var(--color-tint);
    font-weight: 700;
    color: #fff;
  }

  .cart-list {
    position: absolute;
    top: 44px;
    bottom: 49px;
    width: 100%;
  }
</style>
