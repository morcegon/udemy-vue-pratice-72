<template>
  <div class="col-xs-12 col-sm-6">
    <ul class="list-group">
      <app-server
        v-for="server in servers"
        :server='server'
        :key="server.id"></app-server>
    </ul>
  </div>
</template>

<script>
  import Server from './Server.vue'
  export default {
    data: () => {
      return {
        servers: [
          {id: 1, status: 'Critical'},
          {id: 2, status: 'Offline'},
          {id: 3, status: 'Loaded'},
          {id: 4, status: 'Unknow'},
          {id: 5, status: 'Critical'}
        ]
      }
    },
    components: {
      appServer: Server
    }
  }
</script>
