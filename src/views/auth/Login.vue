<template>
  <div>
    <label>
      <input value="账号" />
      <input value="密码" type="password" />
      <input type="button" @click="login()" value="登录" />
    </label>
  </div>
</template>

<script>
import axios from "axios";
axios.defaults.headers.post["Content-Type"] =
  "application/x-www-form-urlencoded";
export default {
  data() {
    return {};
  },
  methods: {
    login() {
      axios.get("").then((res) => {
        alert("请求成功，response=" + res.data);
        // data = res.data;
        console.log(res.data.navList);
      });
    },
  },
};
</script>

<style></style>
