<template>
  <header>
    <h1>{{ propsdata }}</h1>
  </header>
</template>

<script>
export default {
  // instance 옵션
  // 상위 컴포넌트에서 여기의 propsdata로 데이터를 내려줄 수 있다.
  props: ["propsdata"],
};
</script>

<style></style>
