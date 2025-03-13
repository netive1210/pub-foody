<template lang="html">
  <Header/>
  <v-container>
    <v-col cols="12" class="d-flex justify-center">
      <v-avatar size="250">
        <v-img src="/public/images/maru.jpg" class="commonet-p" @click="openFile" />
      </v-avatar>
      <v-file-input class="d-none" label="input profile" ref="profile"></v-file-input>
    </v-col>
    <v-col cols="12">
      <v-text-field v-model="id" color="primary" label="아이디" variant="underlined"></v-text-field>
      <v-text-field v-model="password" color="primary" label="비밀번호" placeholder="Enter your password"
        variant="underlined"></v-text-field>
      <v-text-field v-model="password_check" color="primary" label="비밀번호 확인" placeholder="Enter your password"
        variant="underlined"></v-text-field>
      <v-text-field v-model="neck" color="primary" label="별명" variant="underlined"
        hint="한글,영어,숫자,특수문자( @, 점(.) 마이너스(-) 밑줄( _ ) )" persistent-hint></v-text-field>
      <v-text-field v-model="email" color="primary" label="이메일" variant="underlined"></v-text-field>
      <v-text-field v-model="id" color="primary" label="이름" variant="underlined"></v-text-field>
    </v-col>

    <v-col cols="12">
      <v-btn color="#ffca28" rounded="xl" size="x-large" block>회원가입</v-btn>
    </v-col>

  </v-container>

</template>
<script setup lang="ts">
import {ref} from 'vue'
const profile = ref(null);
const openFile = function () {
  profile.value.$el.querySelector('input').click();
}
</script>
<style></style>