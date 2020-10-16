<template>
  <img alt="Vue logo" src="../assets/logo.png" />
  <!-- <HelloWorld msg="Welcome to Your Vue.js + TypeScript App" /> -->
  <ModalButton />
</template>

<script lang="ts">
import { defineComponent, SetupContext } from "vue";
import ModalButton from "@/components/ModalButton.vue";
import router from "@/router";
import store from "@/store";

export default defineComponent({
  name: "Home",
  components: {
    // HelloWorld,
    ModalButton,
  },
  setup(_, context: SetupContext) {
    return {};
  },
});
</script>
