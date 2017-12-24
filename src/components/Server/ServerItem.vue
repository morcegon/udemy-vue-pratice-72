<template>
  <div>
    <li
      class="list-group-item">
      Server #{{ serverInfo.id }}
    </li>
  </div>
</template>

<script>
  export default {
    props: {
      serverInfo: Object
    }
  }
</script>
