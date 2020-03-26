<template>
    <div>
        <van-nav-bar
  title="登录"
/>
        <van-form @submit="onSubmit">
  <van-field
    v-model="username"
    left-icon="contact"
    name="用户名"
    placeholder="用户名"
    :rules="[{ required: true, message: '请填写用户名' }]"
  />
  <van-col span="16">
      <van-field
    v-model="password"
    left-icon="setting-o"
    type="password"
    name="密码"
    placeholder="密码"
    :rules="[{ required: true, message: '请填写密码' }]"
  />
  </van-col>
 
  <van-button round size="mini">发送验证码</van-button>
  <div style="margin: 16px;">
    <van-button round block type="info" native-type="submit">
      提交
    </van-button>
  </div>
</van-form>
    </div>
</template>
<script>
export default {
  data () {
    return {
      username: '',
      password: '',
    }
  },
  methods: {
    onSubmit (values) {
      console.log('submit', values)
    }
  }
}
</script>
<style lang="less" scoped>
.van-nav-bar{
  background: #1989fa;
  color: #fff;
  .van-nav-bar__title{
      color: #fff;
  }
}
</style>
