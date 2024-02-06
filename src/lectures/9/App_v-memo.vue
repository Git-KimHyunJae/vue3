<template>
  <div>
    <div v-memo="[subscibers]">
      <p>subscibers:{{ subscibers }}</p>
      <p>views:{{ views }}</p>
      <p>likes:{{ likes }}</p>
    </div>
    <button @click="subscibers++">Subs++</button>
    <button @click="views++">Views++</button>
    <button @click="likes++">Likes++</button>
    <div>
      <p>subscibers:{{ subscibers }}</p>
      <p>views:{{ views }}</p>
      <p>likes:{{ likes }}</p>
    </div>
  </div>
</template>

<script>
import { ref } from 'vue'
export default {
  setup() {
    const subscibers = ref(4000)
    const views = ref(400)
    const likes = ref(20)
    return {
      subscibers,
      views,
      likes
    }
  }
}
</script>

<style lang="scss" scoped></style>
