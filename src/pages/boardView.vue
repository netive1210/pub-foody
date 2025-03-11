<template>
  <Header />
  <v-carousel height="400" show-arrows="hover" cycle>
    <v-carousel-item v-for="(img, i) in imgs" :key="i" :src="img" cover></v-carousel-item>
  </v-carousel>
  <v-card>
    <v-card-title class="text-h6">고양이 너무기여어</v-card-title>
    <v-card-subtitle class="w-info d-flex justify-space-between ">
      <span class="cate">디저트 > 케이크</span>
      <span class="line-norwap nick">일이삼사오육칠팔구십일이삼사오</span>
    </v-card-subtitle>
    <v-card-subtitle class="w-subinfo text-end">
      <span class="comment">댓글 : 100</span>
      <span class="recommend mr1">추천 : 100</span>
      <span class="view">조회 : 100</span>
      <span class="regDate">2025.02.28</span>
    </v-card-subtitle>
  </v-card>
  <v-col>
    고양이는 식육목 고양이과에 속하는 포유류이다.<br>
    집고양이의 기원은 약 1만년 전 중동 지역에서 스스로 숲속을 나와 사람들이 모여사는 마을에 정착하여 길들여진 아프리카들고양이로 추측된다.<br>
    최근 고고학과 유전학의 발전에 따르면 고양이의 가축화는 기원전 7500년경 근동 지역에서 발생했다.
  </v-col>
  <v-col>
    <v-icon>mdi-map-marker</v-icon>
    서울 마포구 월드컵북로 63
  </v-col>
  <KakaoMap :lat="coordinate.lat" :lng="coordinate.lng" :draggable="true" :width="coordinate.width"
    :height="coordinate.hegiht" :level="coordinate.level">
    <KakaoMapMarker :lat="coordinate.lat" :lng="coordinate.lng"></KakaoMapMarker>
  </KakaoMap>
  <v-row no-gutters>
    <v-col cols="2">
      <v-btn prepend-icon="mdi-skull" stacked variant="plain">
        신고
      </v-btn>
    </v-col>
    <v-col cols="10" class="text-right">
      <v-btn prepend-icon="mdi-heart-minus" stacked variant="plain">
        비추천
      </v-btn>
      <v-btn prepend-icon="mdi-heart-plus" stacked variant="plain">
        추천
      </v-btn>
    </v-col>
  </v-row>

  <Comment/>
  
</template>

<script setup lang="ts">
import { useKakao } from 'vue3-kakao-maps/@utils';
import { KakaoMap, KakaoMapMarker } from 'vue3-kakao-maps';
import Comment from '@/components/Comment.vue';
useKakao('7359fa27627851cf25e1165696659164')

const coordinate = {
  lat: 37.55946053139,
  lng: 126.916653657745,
  width: '100%',
  hegiht: '200px',
  level: 3,
}

const imgs = [
  '/public/images/1.jpg',
  '/public/images/2.jpg',
  '/public/images/3.jpg',
  '/public/images/4.jpg',
  '/public/images/5.png',
]


</script>

<style></style>