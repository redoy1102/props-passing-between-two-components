<template>
  <div>
    <div v-for="b in book" :key="b">
      <p><b>Title-</b>{{ b.id }} {{ b.title }}</p>
    </div>
  </div>
</template>

<script>
export default {
  props: ['book'],
}
</script>