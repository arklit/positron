
<template>
  <div class="main">
    <sum-box
    :summCount="summCount"
    :summTotal="summTotal"/>
    <breadcrumbs-elem/>
    <div class="main__wrapper">
      <cart-main
      :summCount="summCount"/>
      <cart-total
      :summTotal="summTotal"
      :summCount="summCount"
      :install="true"/>
    </div>
  </div>
</template>

<script>
import SumBox from '@/components/SumBox.vue'
import BreadcrumbsElem from '@/components/BreadcrumbsElem.vue';
import CartMain from "@/components/СartMain.vue";
import CartTotal from '@/components/СartTotal.vue';
export default {
  components: {
    SumBox, BreadcrumbsElem, CartMain, CartTotal
  },
  data() {
    return  {
      summa: 10000,
      summCount: 1,
      summTotal: 10000,
      install: true,
    }
  },
}
</script>

<style lang="scss">
@import url('https://fonts.googleapis.com/css2?family=Lato:wght@400;700;900&family=Prata&display=swap');

html {
  box-sizing: border-box;
  height: 100%;
  scroll-behavior: smooth;
}

*::before,
*::after {
  box-sizing: inherit;
}
* {
margin: 0;
box-sizing: border-box;
}
body {
  padding: 0;
  margin: 0;

  display: flex;
  flex-direction: column;
  min-height: 100vh;
  font-size: var(--size-normal);
  line-height: 1.4;
  color: var(--color-black);
  font-weight: var(--font-regular);
}
main {
  flex-grow: 1;
}

a {
  text-decoration: none;
  cursor: pointer;
}

footer {
  flex-shrink: 0;
}
button {
  border: none;
  background: transparent;
  cursor: pointer;
}

img {
  max-width: 100%;
  height: auto;
  display: block;
}

ul {
  list-style: none;
  padding: 0;
}

input {
  border: none;
  outline: none;
  padding: 0;
}
.main {
  padding: 0 80px;
  display: flex;
  flex-direction: column;
  font-family: "Lato", sans-serif;

  &__wrapper {
    display: flex;
    align-items: center;
    justify-content: space-between;
    gap: 55px;
  }
}

</style>
