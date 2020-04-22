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
.container {
  min-height: 100vh;
  display: flex;
  justify-content: center;
  align-items: center;
  text-align: center;
}

.title {
  font-family: "Quicksand", "Source Sans Pro", -apple-system, BlinkMacSystemFont, "Segoe UI", Roboto, "Helvetica Neue", Arial, sans-serif; /* 1 */
  display: block;
  font-weight: 300;
  font-size: 100px;
  color: #35495e;
  letter-spacing: 1px;
}

.subtitle {
  font-weight: 300;
  font-size: 42px;
  color: #526488;
  word-spacing: 5px;
  padding-bottom: 15px;
}

.links {
  padding-top: 15px;
}
</style>
