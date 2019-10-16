<template lang="html">
    <li v-on:click="handleClick">{{countryprop.name}}</li>
</template>

<script>
import { eventBus } from '../main.js'

export default {
  name: 'list-item',
  props: ['countryprop'],
  methods: {
    handleClick() {
      eventBus.$emit('country-selected', this.countryprop);
    }
  }
}
</script>

<style lang="css" scoped>
</style>
