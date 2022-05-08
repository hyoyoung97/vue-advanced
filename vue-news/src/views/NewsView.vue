<template>
  <div>
    <div v-for="user in users">{{ user }}</div>
  </div>
</template>

<script>
export default {
  name: 'NewsView',
  data() {
    return {
      users: []
    }
  },
  created() {
    this.$store.dispatch('FETCH_NEWS');

    // var vm = this;
    // fetchNewsList()
    //     .then(function (response) {
    //       vm.users = response.data;
    //     })
    //     .catch(function (error) {
    //       console.log(error);
    //     })
  }
}
</script>

<style scoped>

</style>