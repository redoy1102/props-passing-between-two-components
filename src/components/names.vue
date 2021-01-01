<template>
  <div>
  <div v-for="(n,id) in name" :key="id">
    <p>{{ n.body }}</p>
  </div>
  </div>
</template>

<script>
export default {
  props: ['name'],
}
</script>