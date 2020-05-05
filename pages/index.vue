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
        :items="catalogElements"
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
                link: '/images/sliders/1.jpg',
                title: 'ССК “ОЛИМП”',
                decription: 'Световое оформление форума “Шубы-2019”'
              },
              {
                link: '/images/sliders/2.jpg',
                title: 'ССК “Молодец”',
                decription: 'Музыкальное оформление форума “Шубы-2019” и Световое оформление форума “Шубы-2019”'
              },
              {
                link: '/images/sliders/1.jpg',
                title: 'Тест',
                decription: 'Description Description'
              },
              {
                link: '/images/sliders/2.jpg',
                title: 'Title2',
                decription: '111111111'
              }
            ],
            titleCatalog: 'Каталог продукции',
            catalogElements: [
                {
                    tabName: 'Robe',
                    elements: [
                        {
                            id: 1,
                            img: '/images/sliders/2.jpg',
                            decription: 'Статичные светодиодные приборы'
                        },
                        {
                            id: 2,
                            img: '/images/sliders/2.jpg',
                            decription: 'Контроллеры'
                        },
                        {
                            id: 3,
                            img: '/images/sliders/2.jpg',
                            decription: 'Аксессуары'
                        }
                    ]
                },
                {
                    tabName: 'Compulite',
                    elements: [
                        {
                            id: 4,
                            img: '/images/sliders/1.jpg',
                            decription: 'Статичные светодиодные приборы'
                        },
                        {
                            id: 5,
                            img: '/images/sliders/1.jpg',
                            decription: 'Контроллеры'
                        },
                        {
                            id: 6,
                            img: '/images/sliders/1.jpg',
                            decription: 'Аксессуары'
                        }
                    ]
                },
            ]
        }
    }
}
</script>

<style>
</style>
