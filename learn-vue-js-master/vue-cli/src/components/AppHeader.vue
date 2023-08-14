<template>
  <header>
    <h1>{{ propsdata }}</h1>
    <!-- event emit -->
    <!-- <button v-on:click="실행할 메서드 이름">send</button> -->
    <button v-on:click="sendEvent">send</button>
  </header>
</template>

<script>
export default {
  // instance 옵션
  // 상위 컴포넌트에서 여기의 propsdata로 데이터를 내려줄 수 있다.
  props: ["propsdata"],
  methods: {
    sendEvent: function () {
      // this.$emit(정의한 이벤트)
      // 정의한 이벤트가 상위 컴포넌트로 전달이 된다.
      this.$emit("renew");
    },
  },
};
</script>

<style></style>
