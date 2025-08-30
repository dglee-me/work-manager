<template>
  <v-app-bar :elevation="0">
    <v-app-bar-title class="font-weight-bold text-h5">Fide</v-app-bar-title>
    <Divider />
    <template #append>
      <v-btn :ripple="false" slim="true" style="border-color: #C9CDCF;" variant="outlined">로그인 / 회원가입</v-btn>
    </template>
  </v-app-bar>
</template>
