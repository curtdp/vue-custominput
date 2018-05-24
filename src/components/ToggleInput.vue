<template>
  <span class="toggle flex-no-shrink" role="checkbox" tabindex="0"
    :aria-checked="value.toString()"
    @click="toggle"
    @keydown.space.prevent="toggle"
  ></span>
</template>

<script>
  export default {
    data() {
      return {
        value: false
      }
    },
    methods: {
      toggle() {
        this.value = !this.value
      }
    }
  }
</script>

<style scoped>

</style>