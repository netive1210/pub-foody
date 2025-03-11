<template>
    <v-app-bar :elevation="2">
        <template v-slot:prepend>
            <v-btn icon>
                <v-icon>mdi-arrow-left</v-icon>
            </v-btn>
        </template>
        <v-app-bar-title></v-app-bar-title>
        <template v-slot:append>
            <v-btn icon>
                <v-icon>mdi-magnify</v-icon>
            </v-btn>
            <v-btn icon>
                <v-icon>mdi-menu</v-icon>
            </v-btn>
        </template>
    </v-app-bar>
</template>
<script lang="ts">
export default {

}
</script>
<style lang="">

</style>