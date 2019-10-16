<template lang="html">
  <div>
    <h1>All countries</h1>
    <ul>
        <list-item v-for="(country, index) in countriesprop" :key="index" :countryprop="country"></list-item>
    </ul>
  </div>
</template>

<script>
import ListItem from './ListItem.vue';

export default {
  name: 'countries-list',
  props: ['countriesprop'],
  components: {
    "list-item": ListItem
  }
}
</script>

<style lang="css" scoped>
</style>
