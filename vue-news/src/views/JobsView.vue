<template>
  <div>
    <div v-for="item in jobs">{{ item.title }}</div>
  </div>
</template>

<script>
export default {
  data() {
    return {
      jobs: []
    }
  },
  created() {
    this.$store.dispatch('FETCH_JOBS');
  }
}
</script>

<style scoped>

</style>