<template lang="html">
  <Header />

  <v-container>
    <v-col>
      <v-text-field v-model="id" color="primary" label="아이디" variant="underlined"></v-text-field>
      <v-text-field v-model="password" color="primary" label="비밀번호" placeholder="Enter your password"
        variant="underlined"></v-text-field>
    </v-col>

    <v-row no-gutters>
      <v-col cols="5" class="d-flex justify-left m-0 p-0 ">
        <v-checkbox color="orange" label="아이디 저장" density="compact" style="transform: scale(0.8);"></v-checkbox>
      </v-col>


    </v-row>

    <v-col>
      <v-btn color="#ffca28" rounded="xl" size="x-large" block>로그인</v-btn>
    </v-col>

    <v-col cols="12" class="d-flex justify-center  m-0 p-0 ">
      <span class="user-span">회원가입</span>
      <span class="user-span">아이디 찾기</span>
      <span class="user-span">비밀번호 찾기</span>
    </v-col>


  </v-container>

</template>
<script setup lang="ts">
import { ref } from 'vue'
</script>
<style>
.user-span {
  font-size: 12px;
}

.user-span:not(:last-child)::after {
  content: '|';
  margin: 0 3px 0 3px
}
</style>