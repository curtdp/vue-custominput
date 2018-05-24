<template>
  <span class="toggle flex-no-shrink" role="checkbox" tabindex="0"
    :aria-checked="receiveNewsletter.toString()"
    @click="toggleNewsletter"
    @keydown.space.prevent="toggleNewsletter"
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