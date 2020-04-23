<template>
    <section class="first-block container">
        <div class="first-block__line">
        </div>
        <div class="first-block__info">
          <h1 class="first-block__title" v-html="title"></h1>
          <div class="first-block__description" v-html="decription"></div>
          <div class="first-block__button">
              <a href="#">ПЕРЕЙТИ</a>
          </div>
        </div>
    </section>
</template>

<script>
  export default {
      name: 'FirstBlock',
      props: {
          title: String,
          decription: String
      }
  }
</script>

<style lang="sass" scoped>
.first-block
    height: 800px
    background: url(~@/assets/images/bg/Rectangle1.jpg)
    background-size: cover
    background-repeat: no-repeat
    background-position: center center
    position: relative

    &__line
        background-color: rgba(#005bc1, 0.6)
        position: absolute
        height: calc(100% - 80px)
        width: 444px
        left: 50%
        bottom: 0
        transform: translateX(-100%)

    &__info
        max-width: 635px
        width: 100%
        position: absolute
        left: 50%
        top: 50%
        transform: translate(-50%, -50%)

    &__title
        font-size: 48px
        color: #fff
        line-height: 71px
        font-family: Oswald
        font-style: normal
        font-weight: normal

    &__description
        font-size: 16px
        line-height: 22px
        color: #fff
        margin-top: 40px

    &__button
        margin-top: 40px
        a
            transition: .3s background-color, .3s color
            min-width: 160px
            height: 51px
            padding: 0 15px
            display: inline-flex
            align-items: center
            justify-content: center
            border: 2px solid #FFFFFF
            box-sizing: border-box
            color: #fff
            text-decoration: none
            &:hover
                background-color: #fff
                color: #005bc1

</style>
