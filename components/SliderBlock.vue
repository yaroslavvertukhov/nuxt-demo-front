<template>
    <section class="slider-block container">
        <div class="slider-block__top-block">
            <div class="slider-block__title">
                <div class="slider-block__title-icon">
                    <img src="~/assets/images/icons/decor-heading.svg" alt="">
                </div>
                <div class="slider-block__title-text">
                    {{ title }}
                </div>
            </div>
            <div class="slider-block__right-block">
                <!-- здесь место под стрелки управления -->
            </div>
        </div>
    </section>
</template>

<script>
    export default {
        name: 'SliderBlock',
        props: {
            title: String
        }
    }
</script>

<style lang="sass" scoped>
    .slider-block
        margin-top: 156px

        &__title
            display: inline-flex
            align-items: center

        &__top-block
            display: flex
            justify-content: space-between

        &__title-icon
            width: 100px

        &__title-text
            font-family: Oswald
            margin-left: 40px
            font-size: 30px
            line-height: 44px
            letter-spacing: 0.05em
            text-transform: uppercase
</style>
