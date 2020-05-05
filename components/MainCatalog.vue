<template>
  <section class="main-catalog container">
    <block-title
      :title="title"
    />
    <div class="main-catalog-tabs">
        <div class="main-catalog-tabs__buttons">
            <div v-for="(item, index) in items" :key="index" class="main-catalog-tabs__button" @click="toggleItem(index)">
                {{ item.tabName }}
            </div>
        </div>
        <transition>
            <div class="main-catalog-tabs__items" name="list" :key="tab.tab">
                <div class="main-catalog-tabs__item" v-for="(item, index) in tab.elements" :key="index">
                    <img :src="item.img" alt="">
                    <span>{{ item.description }}</span>
                </div>
            </div>
        </transition>
    </div>
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
      title: String,
      items: Array
    },
    data() {
        return {
            activeTab: 0
        }
    },
    computed: {
        tab: function() {
            return this.items[this.activeTab];
        }
    },
    methods: {
        toggleItem(index) {
            this.activeTab = index;
        }
    }
  }
</script>

<style lang="sass" scoped>
.main-catalog
  margin-top: 156px

  .list-item
    display: inline-block
    margin-right: 10px

  .list-enter-active, .list-leave-active
    transition: all 1s

  .list-enter, .list-leave-to
    opacity: 0
    transform: translateY(30px)

.list-leave-to
    position: absolute


.main-catalog-tabs
    &__items
        display: flex
    &__item
        img
            width: 100%


</style>
