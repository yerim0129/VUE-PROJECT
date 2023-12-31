<template>
  <modal-layout>
    <template #header>
      <h1>팝업 타이틀</h1>
    </template>
    <!-- slot에 name이 없으면 v-slot:default로 쓴다 -->
    <template v-slot:default>
      <p>팝업 컨텐츠 1</p>
      <p>팝업 컨텐츠 2</p>
    </template>

    <template v-slot:footer>
      <button type="button">닫기</button>
    </template>
  </modal-layout>
</template>
<script>
import ModalLayout from "./SlotModalLayout";

export default {
  components: { ModalLayout },
};
</script>