<template>
  <h3>Home页</h3>
  <img alt="Vue logo" src="@/assets/logo.png">
  <router-link to="/home/detail">Go to Detail</router-link>
  <p>Vuex-count: {{ count }}</p>
</template>

<script lang="ts">
import { defineComponent, computed } from 'vue'
import { useStore } from 'vuex'

export default defineComponent({
  setup() {
    const store = useStore()
    const count = computed(() => store.state.count)
    return { count }
  }
})
</script>

