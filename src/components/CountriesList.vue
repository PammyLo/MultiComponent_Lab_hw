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
import CountrySelect from './CountrySelect.vue';

export default {
  name: 'countries-list',
  props: ['countriesprop'],
  components: {
    "list-item": ListItem,
    "country-select": CountrySelect
  }
}
</script>

<style lang="css" scoped>
</style>
