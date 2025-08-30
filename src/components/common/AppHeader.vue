<template>
  <v-app-bar elevation="0">
    <template #prepend>
      <v-app-bar-nav-icon />
    </template>
    <v-app-bar-title> <AppLogo /> </v-app-bar-title>
    <template #append>
      <!-- 검색 버튼 -->
      <v-btn class="mr-2" variant="outlined">
        <v-icon start>mdi-magnify</v-icon>
        검색
        <span
          class="ml-2 text-caption text-medium-emphasis bg-grey-lighten-2 pl-2 pr-2 rounded-sm"
          >⌘+K</span
        >
      </v-btn>
      <!-- 알림 버튼 -->
      <v-btn class="mr-2" icon variant="text">
        <v-badge location="top right" color="error" content="1">
          <v-icon>mdi-bell-outline</v-icon>
        </v-badge>
      </v-btn>
      <!-- 프로필 버튼 -->
      <v-avatar color="primary">동근</v-avatar>
    </template>
  </v-app-bar>
</template>
