<template>
  <v-app-bar :elevation="0">
    <v-app-bar-title class="font-weight-bold text-h5"><AppLogo /></v-app-bar-title>
    <Divider />
    <template #append>
      <v-btn
        :ripple="false"
        slim="true"
        style="border-color: #c9cdcf"
        to="/login"
        variant="outlined"
      >로그인 / 회원가입</v-btn>
    </template>
  </v-app-bar>
</template>
