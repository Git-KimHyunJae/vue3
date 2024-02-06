<template>
  <div>
    <form action="">
      <input v-model="title" type="text" placeholder="title" />
      <textarea v-model="contents" placeholder="Contents"></textarea>
    </form>
  </div>
</template>

<script>
import { ref, watchEffect } from 'vue'
export default {
  setup() {
    const title = ref('')
    const contents = ref('')
    const save = (title, contents) => {
      console.log(`저장되었습니다. title: ${title}, contents: ${contents}`)
    }
    watchEffect(() => {
      console.log('title.value', title.value)
      save(title.value, contents.value)
      console.log('Contents.value', contents.value)
    })
    return {
      title,
      contents
    }
  }
}
</script>

<style lang="scss" scoped></style>
