<template>
  <h2>{{ Title }}</h2>
</template>
<script>
export default {
  props: {
    Title: {
      type: String,
      default: "페이지 제목입니다.",
    },
  },
};
</script>
