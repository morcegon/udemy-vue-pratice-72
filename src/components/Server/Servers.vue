<template>
  <div class="col-xs-12 col-sm-6">
    <ul class="list-group">
      <server-item
        v-for="server in servers"
        :serverInfo='server'
        :key="server.id"></server-item>
    </ul>
  </div>
</template>

<script>
  import ServerItem from './ServerItem.vue'
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
      serverItem: ServerItem
    }
  }
</script>
