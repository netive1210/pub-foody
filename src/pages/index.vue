<template>
  <v-card class="mx-auto" width="100%">
    <v-list >
      <v-list-group v-for="(item, index) in items" :key="index" :value="item.title">
        <template v-slot:activator="{props}">
          <v-list-item  v-bind:="props" :title="item.title"></v-list-item>
        </template>
        <v-list-item v-for="(children, subidx) in item.children" :key="subidx" :title="children.title"
          :to="children.link">
        </v-list-item>
      </v-list-group>
    </v-list>
  </v-card>
</template>

<script lang="ts" setup>
const items = [
  {
    title: '게시판', children: [
      { title: '목록', link: '/boardList' },
      { title: '상세', link: '/boardView' },
      { title: '댓글 컴포넌트', link: '/commentComp' },
    ]
  },
  { title: '로그인', children: [{ title: '목록', link: '/login' }] },
]
</script>
