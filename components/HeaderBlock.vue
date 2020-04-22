<template>
    <div class="header">
        <div class="header__logo">
            <img src="~/assets/images/logo/logo.svg" alt="">
        </div>
        <div class="header__items">
            <div v-for="(item, index) in items" :key="index" class="header__item">
                <a href="#">{{ item }}</a>
            </div>
        </div>
    </div>
</template>

<script>
  export default {
      name: 'HeaderBlock',
      props: {
         items: {
            type: Array
         }
      }
  }
</script>

<style lang="sass" scoped>

.header
    background-color: rgba(#005bc1, 0.6)
    height: 80px
    display: flex
    justify-content: center
    align-items: center
    position: absolute
    top: 0
    width: 100%
    z-index: 3


    &__logo
        position: absolute
        left: 40px

    &__items
        display: flex

    &__item
        margin: 0 13px

        a
          color: #fff
          text-decoration: none
          font-weight: 600
          font-size: 14px
          position: relative
          &::before
              content: " "
              position: absolute
              transition: .3s width
              width: 0%
              height: 2px
              background-color: #fff
              bottom: 0
              transform: translateY(100%)
          &:hover
              &::before
                  width: 100%

</style>
