<template>


    <v-list-item>

        <!-- 로그인 했을 때  -->
        <!-- <v-row justify="space-between">
            <v-col cols="auto">
                <v-btn icon="mdi-logout"></v-btn>
                <v-btn icon="mdi-cog"></v-btn>
            </v-col>
            <v-col cols="auto">
                <v-btn icon="mdi-close"></v-btn>
            </v-col>
        </v-row>

        <v-list>
            <v-list-item prepend-avatar="/public/images/maru.jpg" subtitle="[등급]" title="@닉네임">
            </v-list-item>
        </v-list> 
        
        
        <v-divider></v-divider>
        -->
        <!-- 로그인 했을 때  -->



        <!-- 로그인 안했을 때 -->
        <v-row justify="space-between">
            <v-col cols="auto">
                <v-btn icon="mdi-login"></v-btn>
                <v-btn icon="mdi-account-plus"></v-btn>
            </v-col>
            <v-col cols="auto">
                <v-btn icon="mdi-close"></v-btn>
            </v-col>
        </v-row>
        <!-- 로그인 안했을 때 -->

    </v-list-item>


</template>
<script>
//등급 
//SILVER :게시물 10이상
//GOLD :게시물 50이상
//PLATINUM :게시물 100이상
//DIAMOND :게시물 1000이상

export default {

}
</script>
<style lang="">

</style>