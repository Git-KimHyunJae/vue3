<template>
  <label class="child-class" style="color: red; border: 1px solid black" id="child-id">
    {{ label }}
    <input
      :value="modelValue"
      @input="(event) => $emit('update:modelValue', event.target.value)"
      type="text"
    />
  </label>
</template>

<script>
// <!--  -->
export default {
  props: ['modelValue', 'label'],
  emit: ['update:modelValue'],
  setup() {
    return {}
  }
}
</script>

<style lang="scss" scoped></style>
