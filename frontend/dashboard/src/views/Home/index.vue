<template>
  <custom-header @create-account="handleAccountCreate" @login="handleLogin" />
  <contact />
  <div class="flex justify-center py-10 bg-brand-gray">
    <p class="font-medium text-center text-gray-800">FeedBacker © 2023</p>
  </div>
</template>

<script>
import CustomHeader from './CustomHeader.vue'

import Contact from './Contact.vue'

export default {
  components: { CustomHeader, Contact },
  methods: {
    handleLogin() {},
    handleAccountCreate() {}
  },
  mounted() {
    const token = window.localStorage.getItem('token')
    if (token) {
      this.$router.push({ name: 'Feedbacks' })
    }
  }
}
</script>
