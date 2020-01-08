<template>
<div>
  <v-app>
    <v-form>
      <v-text-field
        v-model="username"
        label="laura"
      >
      </v-text-field>
      <v-text-field
        v-model="password"
        label="password"
      >
      </v-text-field>
      <v-btn
        @click="login"
      >
      login
      </v-btn>
    </v-form>
  </v-app>
</div>
</template>

<script>
import axios from 'axios';
export default {
  methods: {
    login() {
      let bodyFormData = new FormData();
      bodyFormData.set('username', 'laura');
      bodyFormData.set('password', 'maxwit');
      axios({
        method:'post',
        url:'http://localhost:8080/login',
        data: bodyFormData,
        headers: {'Content-Type': 'multipart/form-data',}
        })
    }
  }
}
</script>
