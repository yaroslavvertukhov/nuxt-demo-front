<template>
  <main>
      <first-block
        :title="siteTitle"
        :decription="siteDecription"
      />
      <slider-block
        :title="sliderBlock"
        :slides="mainSlides"
      />
      <main-catalog
        :title="titleCatalog"
      />
  </main>
</template>

<script>
import FirstBlock from '~/components/FirstBlock.vue'
import SliderBlock from '~/components/SliderBlock.vue'
import MainCatalog from '~/components/MainCatalog.vue'

export default {
    components: {
        FirstBlock,
        SliderBlock,
        MainCatalog
    },
    data() {
        return {
            siteTitle: 'Светотехническое оборудование<br> в Петербурге',
            siteDecription: 'Продажа, аренда светотехнического оборудования.<br> Оформление официальных мероприятий под ключ.',
            sliderBlock: 'Наши проекты',
            mainSlides: [
              {
                link: '/_nuxt/assets/images/sliders/1.jpg',
                title: 'ССК “ОЛИМП”',
                decription: 'Световое оформление форума “Шубы-2019”'
              },
              {
                link: '/_nuxt/assets/images/sliders/2.jpg',
                title: 'ССК “Молодец”',
                decription: 'Музыкальное оформление форума “Шубы-2019” и Световое оформление форума “Шубы-2019”'
              },
              {
                link: '/_nuxt/assets/images/sliders/1.jpg',
                title: 'Тест',
                decription: 'Description Description'
              },
              {
                link: '/_nuxt/assets/images/sliders/2.jpg',
                title: 'Title2',
                decription: '111111111'
              }
            ],
            titleCatalog: 'Каталог продукции'
        }
    }
}
</script>

<style>
</style>
