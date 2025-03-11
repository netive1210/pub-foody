<template>
    <v-row no-gutters>
        <v-container>
            <v-textarea label="comment.." row-height="15" rows="1" variant="outlined" auto-grow append-icon="mdi-plus-box"
            @click:append="insertComment"></v-textarea>
        </v-container>

        <v-list width="100%">
            <v-list-item>
                <template v-slot:prepend>
                    <v-avatar size="60">
                        <v-img src="/public/images/maru.jpg" class="commonet-p" />
                    </v-avatar>
                </template>
                <v-list-item-action class="mb-1 d-flex justify-space-between"> 
                    <span class="nick">@jjjjjnnnn</span>
                    <span class="date">2025.03.06</span>
                </v-list-item-action>
                <v-list-item-action>
                    <small class="mb-1 text-high-emphasis opacity-60">
                        이거슨 댓글 내용이 들어가는 자리입니다.<br>
                        이거슨 댓글 내용이 들어가는 자리입니다.<br>
                        이거슨 댓글 내용이 들어가는 자리입니다.<br>
                        이거슨 댓글 내용이 들어가는 자리입니다.<br>
                    </small>
                </v-list-item-action>
                <v-list-item-action>
                    <span><v-icon size="20">mdi-thumb-up</v-icon> 111</span>
                    <span class="ml-2"><v-icon size="20">mdi-thumb-down</v-icon> 200</span>
                    <span class="ml-10">답글</span>
                </v-list-item-action>
                <v-list-item-action class="mt-5">
                    답글보기
                </v-list-item-action>
                
            </v-list-item>

            <v-container>
                <v-textarea label="comment.." row-height="15" rows="1" variant="outlined" auto-grow append-icon="mdi-plus-box"
                @click:append="insertComment"></v-textarea>
            </v-container>

            <template v-for="i in 5" :key="i">
                <v-list-item class="ml-5">
                <template v-slot:prepend>
                    <v-avatar size="60">
                        <v-img src="/public/images/maru.jpg" class="commonet-p" />
                    </v-avatar>
                </template>
                <v-list-item-action class="mb-1 d-flex justify-space-between"> 
                    <span class="nick">@jjjjjnnnn</span>
                    <span class="date">2025.03.06</span>
                </v-list-item-action>
                <v-list-item-action>
                    <small class="mb-1 text-high-emphasis opacity-60">
                        이거슨 댓글 내용이 들어가는 자리입니다.<br>
                        이거슨 댓글 내용이 들어가는 자리입니다.<br>
                        이거슨 댓글 내용이 들어가는 자리입니다.<br>
                        이거슨 댓글 내용이 들어가는 자리입니다.<br>
                    </small>
                </v-list-item-action>
                <v-list-item-action>
                    <span><v-icon size="20">mdi-thumb-up</v-icon> 111</span>
                    <span class="ml-2"><v-icon size="20">mdi-thumb-down</v-icon> 200</span>
                    <span class="ml-10">답글</span>
                </v-list-item-action>
            </v-list-item>
            
            <v-container v-if="i == 3">
                <v-textarea label="comment.." row-height="15" rows="1" variant="outlined" auto-grow append-icon="mdi-plus-box"
                @click:append="insertComment"></v-textarea>
            </v-container>
            </template>

            

        </v-list>






    </v-row>
</template>


<script setup lang="ts">
const insertComment = () => {
    alert('댓글을 저장해보자.')
}
</script>

<style lang="">

</style>