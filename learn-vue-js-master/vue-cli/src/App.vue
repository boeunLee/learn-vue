<template>
  <div>{{ str }}</div>
</template>

<script>
export default {
  // 기존에 하던 방식과는 다르게 진행되어야함
  // 여러개의 컴포넌트를 만들었을 때 같은 이름을 공유하면 안되기 때문이다.
  // 따라서 function으로 연결해주고 return으로 새 객체를 반환해줘야한다.
  data: function () {
    return {
      str: "hi",
    };
  },
};
</script>

<style></style>
