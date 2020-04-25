<template>
    <section class="slider-block container">
        <block-title
          :title="title"
        >
          <slider-buttons
            @click-prev="prevSlide"
            @click-next="nextSlide"
          />
        </block-title>
        <div class="slider-block__bottom-block">
          <div v-swiper:mainSwiper="swiperOption">
            <div class="swiper-wrapper">
              <div v-for="(item, index) in slides" :key="index" class="swiper-slide slider-block__slide">
                <img :src="item.link" alt="">
                <div class="slider-block__slide-info">
                  <div class="slider-block__slide-title">
                    {{ item.title }}
                  </div>
                  <div class="slider-block__slide-decription">
                    {{ item.decription }}
                  </div>
                </div>
              </div>
            </div>
          </div>
        </div>
    </section>
</template>

<script>
  import BlockTitle from '~/components/BlockTitle.vue';
  import SliderButtons from '~/components/SiderButtons.vue';

  export default {
      name: 'SliderBlock',
      components: {
        SliderButtons,
        BlockTitle
      },
      props: {
          title: String,
          slides: Array
      },
      data() {
        return {
          swiperOption: {
            slidesPerView: 1,
            spaceBetween: 15,
            breakpoints: {
              768: {
                slidesPerView: 2,
              }
            }
          }
        }
      },
      computed: {
       swiper() {
         return this.mainSwiper
       }
      },
      methods: {
        prevSlide() {
          try {
            this.swiper.slidePrev();
          } catch (e) {
            console.error(e);
          }
        },
        nextSlide() {
          try {
            this.swiper.slideNext();
          } catch (e) {
            console.error(e);
          }
        }
      }
  }
</script>

<style lang="sass" scoped>
  .slider-block
    margin-top: 156px

    &__slide
      height: 400px
      position: relative
      img
        object-fit: cover
        width: 100%
        height: 100%

    &__slide-info
      max-width: 250px
      width: 100%
      padding: 20px 25px
      box-sizing: border-box
      background-color: #fff
      position: absolute
      bottom: 35px
      right: 35px
      @media (max-width: 1174px)
        max-width: none
        bottom: 0
        right: 0
        min-height: 124px
        background-color: rgba(#ffffff, 0.9)

    &__slide-title
      font-family: Oswald
      font-size: 18px
      line-height: 27px
      letter-spacing: 0.05em
      text-transform: uppercase

    &__slide-decription
      font-weight: 300
      font-size: 14px
      line-height: 19px
</style>
