<template>
 <div class="cartMain">
   <div class="cartMain__header">
     <h2 class="cartMain__title">Ваша корзина</h2>
     <p class="cartMain__count">{{summCount}} товара</p>
     <button class="cartMain__remove">
      Очистить корзину
     </button>
   </div>
     <div class="cartMain__items">
       <div class="cartMain-item">
        <div class="cartMain-item__photo-box">
          <img src="@/assets/img/item-1.png" alt="item">
          <div class="cartMain-item__content">
            <p class="cartMain-item__name">Вытяжное устройство G2H</p>
            <p class="cartMain-item__stats">12-72/168 м3/ч / гидрорегулируемый расход / от датчика присутствия</p>
            <p class="cartMain-item__articul">Артикул: G2H1065</p>
          </div>
        </div>
        <div class="cartMain-item__box">
          <div class="cartMain-item__counter">
            <div class="cartMain-item__plus">-</div>
            <div class="cartMain-item__count">1</div>
            <div class="cartMain-item__minus">+</div>
          </div>
          <p class="cartMain-item__price-for-item">12 644 ₽/шт. </p>
        </div>
        <div class="cartMain-item__price">25 288 ₽</div>
        <button class="cartMain-item__close">
          <img src="@/assets/img/icons/icon-close.svg" alt="close">
        </button>
       </div>
       <div class="cartMain-item">
        <div class="cartMain-item__photo-box">
          <img src="@/assets/img/item-2.png" alt="item">
          <div class="cartMain-item__content">
            <p class="cartMain-item__name">Вытяжное устройство G2H</p>
            <p class="cartMain-item__stats">12-72/168 м3/ч / гидрорегулируемый расход / от датчика присутствия</p>
            <p class="cartMain-item__articul">Артикул: G2H1065</p>
          </div>
        </div>
        <div class="cartMain-item__box">
          <div class="cartMain-item__counter">
            <div class="cartMain-item__plus">-</div>
            <div class="cartMain-item__count">1</div>
            <div class="cartMain-item__minus">+</div>
          </div>
          <p class="cartMain-item__price-for-item">12 644 ₽/шт. </p>
        </div>
        <div class="cartMain-item__price">25 288 ₽</div>
        <button class="cartMain-item__close">
          <img src="@/assets/img/icons/icon-close.svg" alt="close">
        </button>
       </div>
       <div class="cartMain-item">
        <div class="cartMain-item__photo-box">
          <img src="@/assets/img/item-3.png" alt="item">
          <div class="cartMain-item__content">
            <p class="cartMain-item__name">Вытяжное устройство G2H</p>
            <p class="cartMain-item__stats">12-72/168 м3/ч / гидрорегулируемый расход / от датчика присутствия</p>
            <p class="cartMain-item__articul">Артикул: G2H1065</p>
          </div>
        </div>
        <div class="cartMain-item__box">
          <div class="cartMain-item__counter">
            <div class="cartMain-item__plus">-</div>
            <div class="cartMain-item__count">1</div>
            <div class="cartMain-item__minus">+</div>
          </div>
          <p class="cartMain-item__price-for-item">12 644 ₽/шт. </p>
        </div>
        <div class="cartMain-item__price">25 288 ₽</div>
        <button class="cartMain-item__close">
          <img src="@/assets/img/icons/icon-close.svg" alt="close">
        </button>
       </div>
     </div>
     <check-elem/>
 </div>
</template>


<script>
import CheckElem from "@/components/CheckElem.vue";
export default {
  props: [
    "summCount"
  ],
  components: {
    CheckElem,
  }
}
</script>
<style lang="scss" scoped>

  .cartMain {
    margin-top: 60px;
    width: 100%;
    display: flex;
    flex-direction: column;

    &__header {
      display: flex;
      align-items: flex-end;
    }
    &__title {
      color: #1F2432;
      font-weight: 700;
      font-size: 44px;
      line-height: 120.52%;
    }
    &__count {
      color: #797B86;
      font-weight: 400;
      font-size: 18px;
      line-height: 145%;
      margin-left: 22px;
    }
    &__remove {
      background: transparent;
      padding: 0 0 2px;
      border: none;
      border-bottom: 1px solid #797B86;
      font-weight: 400;
      font-size: 14px;
      line-height: 150%;
      color: #797B86;
      margin-left: auto;
      cursor: pointer;

      &:hover {
        opacity: .5;
      }
    }
    &__items {
      display: grid;
      grid-template-columns: 1fr;
      margin-top: 50px;
    }
    &-item {
      display: flex;
      align-items: center;
      position: relative;
      justify-content: space-between;
      width: 100%;
      padding: 25px 0 23px;
      border-bottom: 1px solid #C4C4C4;

      &:first-child {
        padding-top: 0;

        .cartMain-item__close {
          top: 0;
        }
      }
      

      &__photo-box {
        display: flex;
        flex-direction: row;
        align-items: center;
        gap: 31px;
      }
      &__content {
        display: flex;
        flex-direction: column;
      }
      &__articul {
         font-weight: 400;
         font-size: 14px;
         line-height: 150%;
         color: #797B86;
      }
      &__counter {
        display: flex;
        gap: 3px;

        div {
          background: #F6F8FA;
          border-radius: 4px;
          font-weight: 400;
          font-size: 14px;
          line-height: 150%;
          display: flex;
          justify-content: center;
          align-items: center;
          height: 34px;
          width: 34px;
        }
      }
      &__close {
        position: absolute;
        top: 25px;
        right: 0;
      }
      &__plus, &__minus {
        cursor: pointer;
      }
      &__box {
      display: flex;
      flex-direction: column;
      align-items: center;
      gap: 10px;
      }
      &__price-for-item { 
          font-weight: 600;
          font-size: 12px;
          line-height: 145%;
          text-align: center;
          color: #1F2432;
      }
      &__price {
         font-weight: 600;
         font-size: 18px;
         line-height: 145%;
         color: #1F2432;
      }
    }
  }

</style>