<script>

import { Authenticator } from "@aws-amplify/ui-vue";
import "@aws-amplify/ui-vue/styles.css";

export default {
  name: 'HomeComponents',
  props: {
    msg: String
  }
}
</script>

<template>
    <div class="home">
        <h1>{{ msg }}</h1>
    </div>
    <authenticator>
      <template v-slot="{ signOut }">
        <button @click="signOut">SignOut</button>
      </template>
    </authenticator>  
</template>