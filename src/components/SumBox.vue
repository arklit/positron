<template>
  <div class="summBox">
    <img src="@/assets/img/icons/icon-cart.svg" alt="cart">
    <div class="summBox__info">
      <span class="summBox__title">Ваша Корзина</span>
      <span class="summBox__count">Товара: {{summCount}}</span>
      <span class="summBox__total">{{summTotal}} ₽</span>
    </div>
  </div>
</template>

<script>
export default {
     props: [
     "summCount", "summTotal"
   ],
}
</script>

<style lang="scss" scoped>


.summBox {
  width: 100%;
  display: flex;
  justify-content: flex-end;
  gap: 10px;
  padding: 20px 80px;

  &__info {
    display: flex;
    flex-direction: column;
  }
  &__title {
     font-weight: 400;
     font-size: 14px;
     line-height: 150%;
  }
  &__count {
     font-weight: 400;
     font-size: 12px;
     line-height: 145%;
     color: #797B86;
  }
  &__total {
      font-weight: 400;
     font-size: 14px;
     line-height: 150%;
  }
}

</style>