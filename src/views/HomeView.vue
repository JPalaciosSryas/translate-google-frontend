<template>
  <div class="home">
    <TranslateText msg="Welcome to Your Vue.js App"/>
  </div>
</template>

<script>
// @ is an alias to /src
import TranslateText from '@/components/TranslateText.vue'

export default {
  name: 'HomeView',
  components: {
    TranslateText
  }
}
</script>
