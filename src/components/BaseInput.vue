<template>
  <!-- <div> -->
  <label for="">{{ label }}</label>
  <input
    v-bind="{
      ...$attrs,
      onIuput: (event) => $emit('update:modelValue', $event.target.value),
    }"
    type="email"
    :value="modelValue"
  />
  <!-- </div> -->
</template>

<script>
export default {
  //   inheritAttrs: false,
  emits: [],
  props: {
    modelValue: {
      type: [String, Number],
      default: "",
    },
    label: {
      type: String,
      default: null,
    },
  },
};
</script>

<style scoped></style>
