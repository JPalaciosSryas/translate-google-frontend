<template>
    <div class="web-sites">
      <WebSites />
    </div>
  </template>
  
  <script>
  // @ is an alias to /src
  import WebSites from '@/components/WebSites.vue'
  
  export default {
    name: 'WebSitesView',
    components: {
      WebSites
    }
  }
  </script>