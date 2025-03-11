<template lang="html">
    <Header />

    <template v-for="(item, index) in 20" :key="index">
            <v-card>
                <v-img src="/public/images/maru.jpg" cover></v-img>
                <v-card-title primary-title>타이틀</v-card-title>
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
    </template>


</template>
<script lang="ts">
export default {
}

</script>
<style>
.w-info span {
    display: inline-block;
}
.w-subinfo span:not(:last-child)::after {
    content: '|';
    margin: 0 5px 0 5px
}
</style>