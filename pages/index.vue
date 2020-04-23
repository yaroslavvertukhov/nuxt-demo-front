<template>
  <main>
      <first-block
        :title="siteTitle"
        :decription="siteDecription"
      />
      <slider-block
        :title="sliderBlock"
      />
  </main>
</template>

<script>
import FirstBlock from '~/components/FirstBlock.vue'
import SliderBlock from '~/components/SliderBlock.vue'

export default {
    components: {
        FirstBlock,
        SliderBlock
    },
    data() {
        return {
            siteTitle: 'Светотехническое оборудование<br> в Петербурге',
            siteDecription: 'Продажа, аренда светотехнического оборудования.<br> Оформление официальных мероприятий под ключ.',
            sliderBlock: 'Наши проекты',
        }
    }
}
</script>

<style>
</style>
