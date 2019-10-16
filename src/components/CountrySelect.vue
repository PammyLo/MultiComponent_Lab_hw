<!-- <template lang="html">
  <div>
    <label>Choose a country for more info:</label>
      <select>
        <option disabled value="">select a country</option>
        <option v-on:change="(country, index) in countriesprop" :value="selectedCountry" :key="index">
          {{ country.name }}</option>
      </select>
  </div>
</template>

<script>
import { eventBus } from '../main.js'

export default {
  name: 'country-select',
  props: ['countriesprop'],
  methods: {
    handleChange() {
      eventBus.$emit('country-selected', this.countryprop);
    }
  }
}
</script>

<style lang="css" scoped>
</style> -->
