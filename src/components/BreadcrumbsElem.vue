<template>
  <div class="breadcrumbs">
    <a href="#" class="breadcrumbs__link">Главная</a>
    <a href="#" class="breadcrumbs__link">Корзина</a>
  </div>
</template>
<style lang="scss" scoped>
  .breadcrumbs {
    display: flex;
    gap: 10px;

    a {
      color: #33374E;

      &:first-of-type {
        display: flex;
        gap: 10px;

        &::after {
        content: url('../assets/img/icons/icon-next.svg');
        }
      }
      &:last-of-type {
        color: #797B86;
      }
    }
  }
</style>