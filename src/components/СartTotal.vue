<template>
  <div class="cartTotal">
      <h3 class="cartTotal__header">Итого</h3>
      <div class="cartTotal__summ">
        <p>Сумма заказа</p>
        <p>{{summTotal}} ₽</p>
      </div>
      <div class="cartTotal__count">
        <p>Количество</p>
        <p>{{summCount}} шт</p>
      </div>
      <div class="cartTotal__install">
        <p>Установка</p>
        <p v-if="install">Есть</p>
        <p v-else >Нет</p>
      </div>
      <div class="cartTotal__total cartTotal__summ" v-if="summTotal > 0">
        <p>Стоимость товаров</p>
        <strong><p>{{summTotal}} ₽</p></strong>
      </div>
      <div class="cartTotal__total cartTotal__summ" v-else>
        <strong><p>Корзина пуста</p></strong>
      </div>

      <button class="cartTotal__btn btn">Оформить заказ</button>
      <button class="cartTotal__btn_second btn">Купить в 1 клик</button>
    </div>
</template>
<script>
export default {
   props: [
    "summTotal", "summCount", "install"
   ]
}
</script>
<style lang="scss">

.cartTotal {
  display: flex;
  flex-direction: column;
  align-items: flex-start;
  background: #F6F8FA;
  border-radius: 5px;
  padding: 35px 30px;
  width: 425px;

  &__summ, &__count, &__install, &__total {
    display: flex;
    margin-bottom: 17px;
    justify-content: space-between;
    width: 100%;
  }
  &__header {
    margin-bottom: 30px;
  }
  &__summ {
    padding-top: 10px;
    border-top: 1px solid #AEB0B6;
  }
  .btn {
    padding: 14px 40px;
    border-radius: 4px;
    font-weight: 600;
    font-size: 18px;
    line-height: 145%;
    text-align: center;
    width: 100%;
  }
  &__btn {
     background: #0069B4;
     border: 1px solid transparent;
     color: #FFFFFF;
     margin-bottom: 10px;

     &:hover {
        background: #FFFFFF;
        color: #0069B4;
        border: 1px solid #0069B4;
     }

     &_second {
        background: #FFFFFF;
        color: #0069B4;
        border: 1px solid #0069B4;

        &:hover {
          background: #0069B4;
          border: 1px solid transparent;
          color: #FFFFFF;
        }
     }
  }
}
</style>