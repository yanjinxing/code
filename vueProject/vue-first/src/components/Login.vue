<template>
    <div>
         UserName: <input v-model="message" @blur="bl"/><br/>
         <br/>
         PassWord: <input v-model="passmessage"/><br/>
         <br/>
           <button @click="login">Login</button>
           <p>{{ message }}</p><br/>
           <p>{{ passmessage }}</p>
    </div>
</template>

<script>
export default {
  methods: {
    login () {
      alert('login....')
    },
    bl: function () {
      var reg = /^[a-zA-Z_0-9]+$/
      if (reg.test(this.message)) {
        alert('ok')
      } else {
        alert('请输入字母或者数字')
      }
    }
  },
  data () {
    return {message: '请输入字母或者数字',
      passmessage: '请输入字母或者数字'
    }
  }
}

</script>
