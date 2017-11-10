<template>
  <div class="vue-dropdown" :class="[className]">
    <div class="vue-dropdown-title" :class="titleClassName">
      <slot name="title"></slot>
    </div>
    <div class="vue-dropdown-content">
    <div class="vue-dropdown-text" :class="textClassName">
      <slot name="text"></slot>
    </div>
    </div>
  </div>
</template>
<script type="text/javascript">

  export default {
    props: {
      className: {
        type: String
      },
      titleClassName: {
        type: String
      },
      textClassName: {
        type: String
      }
    },
    methods: {},
    mounted() {

    }
  }

</script>
<style rel="stylesheet/scss" lang="scss">
  .vue-dropdown {
    position: relative;
    &-title {
      position: relative;
      color: #6C6F70;
      font-size: 14px;
      cursor: pointer;
      height: 30px;
      &:after {
        content: '';
        position: absolute;
        left: -20px;
        top: -20px;
        right: -20px;
        bottom: -20px;
      }
    }
    &-content{
      position: relative;
    }
    &-text {
      position: absolute;
      font-size: 12px;
      opacity: 0;
      transition: opacity .3s;
      left: 50%;
      top: 0;
      transform: translate(-50%, 0%);
      margin:10px 0;
      padding: 5px;
      background-color: #fff;
      box-sizing: border-box;
      border-radius: 4px;
      box-shadow: 0 1px 6px rgba(0, 0, 0, .2);
      z-index: 900;
    }
    &:hover {
      .vue-dropdown {
        &-title {
          color: #308697;
        }
        &-text {
          opacity: 1;
        }
      }
    }
  }
</style>
