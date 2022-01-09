<template>
  <v-card outlined max-width="500px">
    <v-card-title>LOG IN</v-card-title>
    <v-list-item>
      <v-list-item-content>
        <Textfield label="EMAIL" :val="username"></Textfield>
        <Textfield
          :show="false"
          :showIcon="true"
          label="PASSWORD"
          :val="password"
        ></Textfield>
        <v-btn block text> LOG IN </v-btn>
      </v-list-item-content>
    </v-list-item>
  </v-card>
</template>

<script>
import { defineComponent, ref } from "@nuxtjs/composition-api";
import Textfield from "~/components/fields/textfield.vue";

export default defineComponent({
  name: "Login",
  components: { Textfield },
  setup() {
    const username = ref("GUEST")
    const password = ref("password")

    return {
      username,
      password,
    }
  }
})
</script>

<style>
</style>