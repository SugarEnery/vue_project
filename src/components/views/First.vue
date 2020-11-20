<template>
  <div class="first-app">
    {{ msg }}
    <confirm text="注册" @message="getMessage"></confirm>
    <router-link to="/second">去第二个页面</router-link>
  </div>
</template>

<script>
import Confirm from '../sub/Confirm'
export default {
  name: 'First',
  components: {
    Confirm
  },
  data () {
    return {
      msg: 'come on!'
    }
  },
  methods: {
    getMessage (val) {
      alert(val)
    }
  }
}
</script>

<style scoped >
.first-app {
  font-size: 30px
}
</style>
