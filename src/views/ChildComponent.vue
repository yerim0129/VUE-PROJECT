<template>
  <button type="button" @click="childFunc" ref="btn">Click</button>
</template>

<script>
export default {
  methods: {
    childFunc() {
      console.log("부모 comp 에서 직접 발생시킨 이벤트");
    },
  },
};
</script>
