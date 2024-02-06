<template>
  <div></div>
</template>

<script>
import { ref, watch, reactive } from 'vue'
export default {
  setup() {
    const x = ref(0)
    const y = ref(0)
    const obj = reactive({
      count: 0,
      name: 'a'
    })
    // watch([x, y], ([newX, newY]) => {
    //   console.log(newX, newY)
    // })
    // watch(
    //   () => [obj.count, obj.name],
    //   (newValue, oldValue) => {
    //     console.log('new', newValue)
    //     console.log('old', oldValue)
    //   }
    // )
    watch(
      () => obj,
      (newValue, oldValue) => {
        console.log('new', newValue)
        console.log('old', oldValue)
      }
    )
    return {
      x,
      y,
      obj
    }
  }
}
</script>

<style lang="scss" scoped></style>
