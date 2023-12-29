<template>
  <child-component @send-message="sendMessage" ref="child_component" />
</template>
<script>
import childComponent from "./ChildComponent";
export default {
  components: { childComponent },
  mounted() {
    this.$refs.child_component.$refs.btn.click();
  },
};
</script>
