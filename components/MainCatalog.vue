<template>
  <section class="main-catalog container">
    <block-title
      :title="title"
    />
  </section>
</template>

<script>
  import BlockTitle from '~/components/BlockTitle.vue';

  export default {
    name: 'MainCatalog',
    components: {
      BlockTitle
    },
    props: {
      title: String
    }
  }
</script>

<style lang="sass" scoped>
.main-catalog
  margin-top: 156px

</style>
