<template lang="html">
  <div>
    <input type="number" v-model="state.input_value" /><br>
    Input value is {{state.input_value}} and its double is {{state.double}}
  </div>
</template>

<script>
import { reactive, computed } from '@vue/composition-api'

export default {
  setup() {
    const state = reactive({
      input_value: 0,
      double: computed(() => state.input_value * 2)
    })

    return {
      state
    }
  }
}
</script>

<style lang="css" scoped>
</style>
