<template lang="html">
<div class="main-container">
  <countries-list :countriesprop='countries'></countries-list>
  <!-- <country-select :countriesprop='countries'></country-select> -->
  <country-detail v-if="selectedCountry" :countryprop='selectedCountry'></country-detail>
</div>

</template>

<script>
import CountriesList from './components/CountriesList.vue';
// import CountrySelect from './components/CountrySelect.vue';
import CountryDetail from './components/CountryDetail.vue';
import {eventBus} from './main.js'

export default {
  name: "app",
  data() {
    return {
      countries: [],
      selectedCountry: null
    };
  },
  mounted(){
      fetch('https://restcountries.eu/rest/v2/all')
      .then(res => res.json())
      .then(data => this.countries = data)

      eventBus.$on('country-selected', (countryprop) => {
          this.selectedCountry = countryprop;
      });
    },
  components: {
    "countries-list": CountriesList,
    // "country-select": CountrySelect,
    "country-detail": CountryDetail
  }
}
</script>

<style lang="css" scoped>
.main-container {
    display: flex;
    justify-content: space-between;
  }
</style>
