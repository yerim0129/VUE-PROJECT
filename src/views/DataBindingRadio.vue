<template>
  <label>
    <input type="radio" v-bind:value="radio1" v-model="picked" />서울
  </label>

  <label>
    <input type="radio" v-bind:value="radio2" v-model="picked" />부산
  </label>
  <label>
    <input type="radio" v-bind:value="radio3" v-model="picked" />제주
  </label>

  <br />

  <span>체크한 지역 : {{ picked }}</span>
</template>

<script>
/* eslint-disable */
export default {
  name: "DataBindingRadio",
  data() {
    return {
      picked: "",
      radio1: "서울",
      radio2: "부산",
      radio3: "광명",
    };
  },
};
</script>
