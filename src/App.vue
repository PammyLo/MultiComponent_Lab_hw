<template lang="html">
<div>
  <h1>Countries</h1>
  <countries-list :countriesprop='countries'></countries-list>
</div>

</template>

<script>
import CountriesList from './components/CountriesList.vue';

export default {
  name: "app",
  data() {
    return {
      countries: []
    }
  },
  mounted(){
      fetch('https://restcountries.eu/rest/v2/all')
      .then(res => res.json())
      .then(data => this.countries = data)

      // eventBus.$on('munro-selected', (munro) => {
      //     this.selectedMunro = munro;
      // });
    },
  components: {
    "countries-list": CountriesList
  }
}
</script>

<style lang="css" scoped>
</style>
