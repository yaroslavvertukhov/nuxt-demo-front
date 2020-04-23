<template>
  <main>
      <first-block
        :title="title"
        :decription="decription"
      />
  </main>
</template>

<script>
import FirstBlock from '~/components/FirstBlock.vue'

export default {
    components: {
        FirstBlock
    },
    data() {
        return {
            title: 'Светотехническое оборудование<br> в Петербурге',
            decription: 'Продажа, аренда светотехнического оборудования.<br> Оформление официальных мероприятий под ключ.'
        }
    }
}
</script>

<style>
</style>
