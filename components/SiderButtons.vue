<template>
  <div class="slider-buttons">
    <div class="slider-buttons__button slider-buttons__button--left" @click="$emit('click-prev')">
      <svg width="12" height="19" viewBox="0 0 12 19" fill="none" xmlns="http://www.w3.org/2000/svg">
        <line x1="1.1024" y1="10.1977" x2="10.0072" y2="1.29292" stroke="#005BC1" stroke-width="2"/>
        <line y1="-1" x2="12.5932" y2="-1" transform="matrix(-0.707107 -0.707107 -0.707107 0.707107 9.90475 19)"  stroke-width="2"/>
      </svg>
    </div>
    <div class="slider-buttons__button slider-buttons__button--right" @click="$emit('click-next')">
      <svg width="12" height="19" viewBox="0 0 12 19" fill="none" xmlns="http://www.w3.org/2000/svg">
        <line y1="-1" x2="12.5932" y2="-1" transform="matrix(-0.707107 -0.707107 -0.707107 0.707107 9.90485 10.9048)" stroke-width="2"/>
        <line x1="1.10246" y1="18.2929" x2="10.0072" y2="9.38813" stroke="#005BC1" stroke-width="2"/>
      </svg>
    </div>
  </div>
</template>

<script>

  export default {
    name: 'SliderButtons'
  }
</script>

<style lang="sass" scoped>
  .slider-buttons
    display: flex

    &__button
      transition: .3s background-color
      border: 2px solid #005BC1
      width: 55px
      height: 55px
      background-color: transparent
      display: flex
      align-items: center
      justify-content: center
      cursor: pointer
      line
        transition: .3s stroke
        stroke: #005BC1
      &:hover
        background-color: #005BC1
        line
          stroke: #fff
      &--right
        border-left: none

</style>
