<template>
  <div class="row">
    <div class="font-weight-medium notice-wrap">{{ title }}</div>
  </div>
</template>
<script lang="ts">
export default {
  data: () => (
    {
      title: '[공지] 비속어 쓰지말라했어쓰지말라했어쓰지말라했어쓰지말라했어쓰지말라했어쓰지말라했어..',
    }
  ),
}
</script>
<style scoped>
.notice-wrap {
  margin: 0;
  padding-left: 5px;
  width: 100%;
  overflow: hidden;
  white-space: nowrap;
  text-overflow: ellipsis;
}
</style>
