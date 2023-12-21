<template>
  <div>
    <img v-bind:src="imgSrc" />
  </div>
</template>

<script>
/* eslint-disable */
export default {
  name: "DataBindingAtrribue",
  data() {
    return {
      imgSrc: "https://kr.vuejs.org/images/logo.png",
    };
  },
};
</script>
