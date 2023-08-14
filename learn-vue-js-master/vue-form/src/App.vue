<template>
  <!-- submit이라는 이벤트가 발생한다. -->
  <form v-on:submit="submitForm">
    <!-- v-model 속성을 사용하면 input에 값을 입력할때마다 자동으로 반영된다. -->
    <div>
      <label for="username">id: </label>
      <input id="username" type="text" v-model="username" />
    </div>
    <div>
      <label for="password">pw: </label>
      <input id="password" type="password" v-model="password" />
    </div>
    <!-- button의 type이 submit이면, input에서의 엔터까지 form에서 입력을 받게 된다. -->
    <!-- 버튼을 클릭하거나 엔터를 눌렀을때 form에서 이벤트가 일어난다. -->
    <button type="submit">login</button>
  </form>
</template>

<script>
export default {
  data: function () {
    return {
      // 여기에 바로 반영된다는 뜻
      username: "",
      password: "",
    };
  },
  methods: {
    submitForm: function (event) {
      // form을 제출하면 바로 새로고침되므로 이를 방지하기 위함
      event.preventDefault();
      console.log(this.username, this.password);
    },
  },
};
</script>

<style></style>
