<template>
  <div class="checkElem">
    <input type="checkbox" name="check" class="checkElem__input">
    <img src="@/assets/img/icons/icon-tools.svg" alt="tools">
    <div class="checkElem__info">
      <p>Установка</p>
      <p>Отметьте, если Вам необходима консультация профессионала по монтажу выбранных товаров.</p>
    </div>
  </div>
</template>
<style lang="scss" scoped>

 .checkElem {
  display: flex;
  align-items: center;
  background: #F6F8FA;
  border-radius: 5px;
  gap: 20px;
  width: 100%;
  padding: 26px 0 26px 25px;
  margin-top: 44px;

  &__info {
    display: flex;
    flex-direction: column;

    p {
      font-weight: 400;
      font-size: 14px;
      line-height: 150%;
      color: #797B86;
      &:first-child {
        font-weight: 600;
        font-size: 16px;
        line-height: 145%;
        color: #1F2432;
      }
    }
  }
 }
</style>