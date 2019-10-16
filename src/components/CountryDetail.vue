<template lang="html">
  <div>
    <h3>{{ countryprop.name }}</h3>
    <p>Capital: {{countryprop.capital}}</p>
    <p>Population: {{countryprop.population}}</p>
  </div>
</template>

<script>
export default {
  name: 'country-detail',
  props: ['countryprop']
}
</script>

<style lang="css" scoped>
</style>
