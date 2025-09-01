<template>
  <v-navigation-drawer border="none" permanent>
    <!-- 업무 쓰기 버튼 -->
    <template #prepend>
      <v-list-item>
        <v-btn block color="primary" elevation="0">새 업무</v-btn>
      </v-list-item>
    </template>
    <v-list>
      <v-list-item
        v-for="(item, index) in items"
        :key="index"
        link
        :prepend-icon="item.icon"
        :title="item.title"
      />
    </v-list>
  </v-navigation-drawer>
</template>

<script setup>

  const items = [
    {title: '전체', icon: "mdi-inbox-full"},
    {title: '내 업무', icon: 'mdi-file-document-outline'},
  ]
</script>
