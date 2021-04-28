<template>
  <div>
    <label v-if="label">{{ label }}</label>
    <input type="text" v-bind="$attrs" v-on="listeners" />
  </div>
</template>

<script>
import { formFieldMixin } from '@/mixins/formFieldMixin.js'

export default {
  mixins: [formFieldMixin],
  computed: {
    listeners() {
      return {
        ...this.$listeners,
        input: this.updateValue,
      }
    },
  },
}
</script>