<template>
  <v-app-bar elevation="0">
    <template #prepend>
      <v-app-bar-nav-icon @click.stop="emit('toggle-drawer')"/>
    </template>
    <v-app-bar-title>
      <AppLogo/>
    </v-app-bar-title>
    <template #append>
      <!-- 검색 버튼 -->
      <v-btn
        class="mr-2"
        style="border-color: #c9cdcf"
        variant="outlined"
      >
        <v-icon start>mdi-magnify</v-icon>
        검색
        <span
          class="ml-2 text-caption text-medium-emphasis bg-grey-lighten-2 pl-2 pr-2 rounded-sm"
        >⌘+K</span>
      </v-btn>
      <!-- 알림 버튼 -->
      <v-tooltip location="bottom" text="알림">
        <template #activator="{ props }">
          <v-btn v-bind="props" class="mr-2" icon variant="text">
            <v-badge color="error" content="1" location="top right">
              <v-icon>mdi-bell-outline</v-icon>
            </v-badge>
          </v-btn>
        </template>
      </v-tooltip>
      <!-- 프로필 버튼 -->
      <v-tooltip location="bottom" text="사용자 정보">
        <template #activator="{props}">
          <v-avatar v-bind="props" color="primary">동근</v-avatar>
        </template>
      </v-tooltip>
    </template>
  </v-app-bar>
</template>

<script setup>
const emit = defineEmits(['toggle-drawer']);
</script>
