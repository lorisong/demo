<!--
 * @Author: your name
 * @Date: 2020-04-08 18:58:56
 * @LastEditTime: 2020-04-08 20:00:46
 * @LastEditors: Please set LastEditors
 * @Description: In User Settings Edit
 * @FilePath: /demo/vue-demo/src/components/HelloWorld.vue
 -->
<template>
  <div>
    <p>用户名：</p>
    <input  @input="phoneNmVerification" :value="phoneNm" type="text" placeholder="必填，只能手机号码" maxlength="11" >
    <p>密码：</p>
    <input  v-model= "password" placeholder="必填，必须包含大小写字母数字及特殊字符">
    <p>真实姓名：</p>
    <input  v-model="realname"  placeholder="必填，只能是中文" maxlength="15">
    <p>邮箱：</p>
    <input v-model= "email" placeholder="选填，填写时验证是否是邮箱格式">
  </div>
</template>

<script>
export default {
  name: 'HelloWorld',
  data() {
    return {
      // username: '123',
      password: '1423',
      realname: '1233',
      email: '1223',
    };
  },
  methods:{
     phoneNmVerification(e){

      e.target.value=e.target.value.replace(/([^0-9])+/g, '');
     
      this.phoneNm = e.target.value;

     },
     
  }
};
</script>


