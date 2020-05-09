<template>
  <section class="main-catalog container">
    <block-title
      :title="title"
    />
    <div class="main-catalog-tabs">
        <div class="main-catalog-tabs__buttons">
            <div
              v-for="(item, index) in items"
              :key="index"
              class="main-catalog-tabs__button"
              :class="{'main-catalog-tabs__button--active': (index === activeTab)}"
              @click="toggleItem(index)"
            >
                {{ item.tabName }}
            </div>
        </div>
        <transition name="list" mode="out-in">
            <div class="main-catalog-tabs__items" v-if="tab" :key="tab.tabName">
                <div class="main-catalog-tabs__item" v-for="(block, index) in tab.elements" :key="index">
                    <img :src="block.img" alt="">
                    <span>{{ block.description }}</span>
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

  .list-enter
    opacity: 0
    transform: translateX(30px)

  .list-leave-to
    opacity: 0
    transform: translateX(-30px)


.list-leave-to
    // position: absolute


.main-catalog-tabs
    &__items
        display: flex
    &__item
        img
            width: 100%
    &__buttons
        display: flex
        justify-content: center
        margin-bottom: 15px

    &__button
        padding: 5px 0
        margin: 0 15px
        box-sizing: border-box
        text-transform: uppercase
        font-family: Oswald
        font-size: 24px
        line-height: 36px
        cursor: pointer
        border-bottom: 2px solid transparent
        &--active
            color: #005BC1
            border-bottom: 2px solid #005BC1


</style>
