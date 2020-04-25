<template>
  <div class="block-title__top-block">
      <div class="block-title__title">
          <div class="block-title__title-icon">
              <img src="~/assets/images/icons/decor-heading.svg" alt="">
          </div>
          <div class="block-title__title-text">
              {{ title }}
          </div>
      </div>
      <div class="block-title__right-block">
        <slot></slot>
      </div>
  </div>
</template>

<script>
  export default {
    name: 'BlockTitle',
    props: {
      title: String
    }
  }
</script>

<style lang="sass" scoped>
.block-title
  &__title
    display: inline-flex
    align-items: center

  &__top-block
    display: flex
    justify-content: space-between
    margin-bottom: 70px
    @media (max-width: 1024px)
      flex-direction: column

  &__title-icon
    width: 100px

  &__title-text
    font-family: Oswald
    margin-left: 40px
    font-size: 30px
    line-height: 44px
    letter-spacing: 0.05em
    text-transform: uppercase

  &__right-block
    @media (max-width: 1024px)
      margin-top: 15px
</style>
