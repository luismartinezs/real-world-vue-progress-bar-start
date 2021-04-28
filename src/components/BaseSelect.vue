<template>
  <div>
    <label v-if="label">{{ label }}</label>
    <select
      :value="value"
      type="text"
      @change="updateValue"
      v-bind="$attrs"
      v-on="$listeners"
    >
      <option
        v-for="option in options"
        :value="option"
        :key="option"
        :selected="option === value"
      >
        {{ option }}
      </option>
    </select>
  </div>
</template>

<script>
import { formFieldMixin } from '@/mixins/formFieldMixin.js'

export default {
  mixins: [formFieldMixin],
  props: {
    options: {
      type: Array,
      require: true,
    },
  },
}
</script>