<template>
  <div>
    <input
        type="radio"
        :checked="modelVAlue === value"
        :value="value"
        @change="$emit('update:modelValue', value)"
        v-bind="$attrs"
    />
    <label v-if="label">{{label}}</label>
  </div>
</template>

<script>
export default {
  props: {
    label: {
      type: String,
      default: ''
    },
    modelVAlue: {
      type: [String, Number],
      default: ''
    },
    value: {
      type: [String, Number],
      required: true
    }
  }
}
</script>
