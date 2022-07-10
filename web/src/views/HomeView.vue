<template>
  <div class="home">
    <webLink msg="Welcome to Your Vue.js App"/>
  </div>
</template>

<script>
// @ is an alias to /src
import webLink from '@/components/webLink.vue'

export default {
  name: 'HomeView',
  components: {
    webLink
  }
}
</script>
