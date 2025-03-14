<template>
    <v-app-bar :elevation="2">
        <template v-slot:prepend>
            <v-btn icon to="/">
                <v-icon>mdi-arrow-left</v-icon>
            </v-btn>
        </template>
        <v-app-bar-title></v-app-bar-title>
        <template v-slot:append>
            <v-btn icon>
                <v-icon>mdi-magnify</v-icon>
            </v-btn>
            <v-btn @click.stop="drawer = !drawer">
                <v-icon>mdi-menu</v-icon>
            </v-btn>
        </template>
    </v-app-bar>

    <v-navigation-drawer v-model="drawer" location="right" temporary>
        <UserInfoComp />
        <v-list-item link title="음식"></v-list-item>
        <v-list-item link title="영상"></v-list-item>
        <v-list-item link title="여행"></v-list-item>
        <v-list-item link title="반려동물"></v-list-item>
    </v-navigation-drawer>

</template>
<script setup lang="ts">
import { ref } from 'vue';
const drawer = ref<boolean>(false);
</script>
<style lang="">

</style>