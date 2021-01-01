<template>
  <div>
    <compNames :name="infos" ></compNames>
    <compInfos :book="infos" ></compInfos>

  </div>
</template>

<script>
import compInfos from './components/Infos'
import compNames from './components/names'
export default {
  data() {
    return {
      infos: [],
    }
  },
  components: {
    compInfos,
    compNames
  },
  created() {
    this.$http.get('https://jsonplaceholder.typicode.com/posts')
        .then((data) => {
          console.log(data)
          this.infos = data.body.slice(0, 5);
        })
  },
}
</script>