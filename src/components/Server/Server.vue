<template>
  <div>
    <li
      class="list-group-item">
      Server #{{ id }}
    </li>
  </div>
</template>

<script>
  export default {
    props: ['id']
  }
</script>
