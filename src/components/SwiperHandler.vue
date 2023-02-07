<template>
  <div class="swiperHandler">
    <div class="swiperHandler__head">
      <h2>Просмотренные товары</h2>
      <div class="swiperHandler__navigation"></div>
    </div>
    <div class="swiperHandler__swiper swiper">
      <div class="swiperHandler__wrapper swiper-wrapper">
        <div class="swiperHandler-item swiper-slide">
          <img src="@/assets/img/swiper-item-1.png" alt="swiper-item">
          <div class="swiperHandler-item__head">
            <p>ВХС</p>
            <p>Вытяжное устройство для механической системы вентиляции</p>
          </div>
          <div class="swiperHandler-item__price">
            <div class="swiperHandler-item__rubles">
              6 848 ₽ – 56 584 ₽ 
            </div>
            <div class="swiperHandler-item__euro">
              77.60 € – 643.86 €
            </div>
          </div>
          <a class="btn">Подробнее</a>
        </div>
                <div class="swiperHandler-item swiper-slide">
          <img src="@/assets/img/swiper-item-2.png" alt="swiper-item">
          <div class="swiperHandler-item__head">
            <p>ВХС</p>
            <p>Вытяжное устройство для механической системы вентиляции</p>
          </div>
          <div class="swiperHandler-item__price">
            <div class="swiperHandler-item__rubles">
              6 848 ₽ – 56 584 ₽ 
            </div>
            <div class="swiperHandler-item__euro">
              77.60 € – 643.86 €
            </div>
          </div>
          <a class="btn">Подробнее</a>
        </div>
                <div class="swiperHandler-item swiper-slide">
          <img src="@/assets/img/swiper-item-3.png" alt="swiper-item">
          <div class="swiperHandler-item__head">
            <p>ВХС</p>
            <p>Вытяжное устройство для механической системы вентиляции</p>
          </div>
          <div class="swiperHandler-item__price">
            <div class="swiperHandler-item__rubles">
              6 848 ₽ – 56 584 ₽ 
            </div>
            <div class="swiperHandler-item__euro">
              77.60 € – 643.86 €
            </div>
          </div>
          <a class="btn">Подробнее</a>
        </div>
                <div class="swiperHandler-item swiper-slide">
          <img src="@/assets/img/swiper-item-4.png" alt="swiper-item">
          <div class="swiperHandler-item__head">
            <p>ВХС</p>
            <p>Вытяжное устройство для механической системы вентиляции</p>
          </div>
          <div class="swiperHandler-item__price">
            <div class="swiperHandler-item__rubles">
              6 848 ₽ – 56 584 ₽ 
            </div>
            <div class="swiperHandler-item__euro">
              77.60 € – 643.86 €
            </div>
          </div>
          <a class="btn">Подробнее</a>
        </div>
      </div>
    </div>
  </div>
</template>
<script>
import Swiper from 'swiper'
import 'swiper/css';
export default {
  mounted() {
    this.swiperEnable()
  },
  methods: {
    swiperEnable() {
      // eslint-disable-next-line no-unused-vars
      const swiper = new Swiper('.swiper', {
        loop: true,
        slidesPerView: 4,
        spaceBetween: 20,
      })
    }
  }
}
</script>
<style lang="scss" scoped>
 .swiperHandler {
  margin-top: 95px;

  h2 {
     font-weight: 600;
     font-size: 30px;
     line-height: 120.52%;
     color: #1F2432;
     margin-bottom: 60px;
  }
  
  &-item {
    background: #F6F8FA;
    display: flex;
    flex-direction: column;
    padding: 25px;
    align-items: center;

    &__head {
      display: flex;
      flex-direction: column;
      gap: 10px;
      
      font-weight: 400;
      font-size: 14px;
      line-height: 145%;
      color: #1F2432;

      p:first-child {
          font-weight: 700;
          font-size: 22px;
          line-height: 120.52%;
          color: #1F2432;
      }
    }
    &__price {
      margin-top: 60px;
      display: flex;
      flex-direction: column;
      align-self: flex-start;
    }
    &__rubles {
        font-weight: 600;
        font-size: 22px;
        line-height: 130%;
        letter-spacing: 0.005em;
        color: #1F2432;
    }
    &__euro {
       font-weight: 400;
       font-size: 16px;
       line-height: 145%;
       color:#8F919B;
    }

    .btn {
    padding: 14px 40px;
    border-radius: 4px;
    font-weight: 600;
    font-size: 18px;
    line-height: 145%;
    text-align: center;
    width: 100%;
    background: #0069B4;
    border: 1px solid transparent;
    color: #FFFFFF;
    margin-top: 20px;
    &:hover {
        background: #FFFFFF;
        color: #0069B4;
        border: 1px solid #0069B4;
     }
    }
  }
 }
</style>