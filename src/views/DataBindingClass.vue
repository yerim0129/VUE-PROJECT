<template>
  <!--<div
    class="container"
    v-bind:class="{ active: isActive, 'text-red': hasError }"
  >
    Class Binding
  </div> -->
  <div
    class="container"
    v-bind:class="[activeClass, errorClass]"
    v-bind:style="styleObj"
  >
    <!-- 배열의 경우 조건에 따른 클래스 바인딩을 할 수 없다 -->
    Class Binding
  </div>
</template>

<script>
/* eslint-disable */
/* input에 텍스트를 입력하는 순간 버튼이 활성화
    v-model=textValue가 비어있는 경우는 버튼이 비활성화 */
export default {
  name: "databindingclass",
  data() {
    // return {
    //   isActive: true,
    //   hasError: false,
    // };
    return {
      activeClass: "active",
      errorClass: "text-red",
      styleObj: {
        textAlign: "left",
        fontSize: "13px",
      },
      //위와 같이 인라인 스타일을 적용하기 위해선 스타일오브젝트를 생성
    };
  },
};
</script>

<style scoped>
.container {
  width: 100%;
  height: 200px;
}

.active {
  background-color: lightcyan;
  font-weight: bold;
}

.text-red {
  color: red;
}
</style>
