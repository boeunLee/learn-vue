<template>
  <div>
    {{ str }}
    <!-- 프롭스 전달 -->
    <!-- <app-header v-bind:하위 컴포넌트에서 정의한 프롭스 속성 이름="상위 컴포넌트의 데이터 이름"></app-header> -->

    <!-- event emit -->
    <!-- v-on:하위 컴포넌트에서 올라온 이벤트 이름="실행할 메서드 이름" -->
    <app-header v-bind:propsdata="str" v-on:renew="renewStr"></app-header>
  </div>
</template>

<script>
import AppHeader from "./components/AppHeader.vue";

export default {
  // 기존에 하던 방식과는 다르게 진행되어야함
  // 여러개의 컴포넌트를 만들었을 때 같은 이름을 공유하면 안되기 때문이다.
  // 따라서 function으로 연결해주고 return으로 새 객체를 반환해줘야한다.
  data: function () {
    return {
      str: "hi",
    };
  },
  components: {
    "app-header": AppHeader,
  },
  methods: {
    renewStr: function () {
      this.str = "hello";
    },
  },
};
</script>

<style></style>
