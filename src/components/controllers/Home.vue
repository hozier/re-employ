<template lang="pug">
    .home HOME
</template>

<script>
export default {
  name: 'home',
  async created() {
    this.isAuthenticated()
  },
  methods: {
    async isAuthenticated() {
      this.authenticated = await this.$auth.isAuthenticated()
      if (this.authenticated) {
        this.$router.push('/dashboard')
      }
    },
  }
}
</script>

