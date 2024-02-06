<template>
  <div>
    <TheNav></TheNav>
    <TheView></TheView>
  </div>
</template>

<script>
import TheNav from './components/TheNav.vue'
import TheView from './components/TheView.vue'
import AppCard from './components/AppCard.vue'
export default {
  components: {
    TheNav,
    TheView,
    AppCard
  },
  setup() {
    return {}
  }
}
</script>
