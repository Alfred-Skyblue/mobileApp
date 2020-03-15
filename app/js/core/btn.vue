<template>
  <div :class="[btnClass, cname]">
    <slot></slot>
  </div>
</template>

<script>
export default {
  name: 'btn',
  props: {
    cname: {
      type: String,
      default() {
        return ''
      }
    }
  },
  data() {
    return {
      btnClass: 'btn'
    }
  }
}
</script>

<style lang="scss" scoped>
@import '../../css/element.scss';
.btn {
  @include btn;
}
</style>
