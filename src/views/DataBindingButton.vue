<template>
  <div>
    <input type="text" v-model="textValue" />
    <button
      type="button"
      v-bind:disabled="textValue == ''"
      @click="clickedalert"
    >
      Clicked
    </button>
  </div>
</template>

<script>
/* eslint-disable */
/* input에 텍스트를 입력하는 순간 버튼이 활성화
    v-model=textValue가 비어있는 경우는 버튼이 비활성화 */
export default {
  name: "databindingbutton",
  data() {
    return {
      textValue: "",
    };
  },
  methods: {
    clickedalert() {
      alert("클릭되었습니다.");
    },
  },
};
</script>
