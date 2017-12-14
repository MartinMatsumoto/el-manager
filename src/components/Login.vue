<template>
  <div class="login">
    <Modal
      v-model="loginShow"
      :closable="closable"
      :mask-closable="maskClosable"
      title="请登录"
      width="500"
      @on-ok="ok">
      <Form ref="formInline" :model="loginForm" :rules="ruleInline" :label-width="40">
        <FormItem label="账号">
          <Input v-model="loginForm.username" placeholder="请输入账号"></Input>
        </FormItem>
        <FormItem label="密码">
          <Input v-model="loginForm.password" placeholder="请输入密码"></Input>
        </FormItem>
      </Form>
    </Modal>
  </div>
</template>

<script>
  import axios from 'axios'
  import TextUtils from './utils/TextUtils.vue'

  export default {
    data () {
      return {
        loginShow: true,
        closable: false,
        maskClosable: false,
        loginForm: {
          username: '',
          password: ''
        },
        ruleInline: {
          user: [
            {required: true, message: 'Please fill in the user name', trigger: 'blur'}
          ],
          password: [
            {required: true, message: 'Please fill in the password.', trigger: 'blur'},
            {type: 'string', min: 6, message: 'The password length cannot be less than 6 bits', trigger: 'blur'}
          ]
        }
      }
    },
    methods: {
      handleSubmit(name) {
        this.$refs[name].validate((valid) => {
          if (valid) {
            this.$Message.success('Success!');
          } else {
            this.$Message.error('Fail!');
          }
        })
      },
      ok : function () {

      },
      cancel : function () {

      }
    }
  }
</script>

<!-- scoped 使得css只在这个vuejs内有效 -->
<style scoped>
</style>
