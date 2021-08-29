<template>
  <div id="app">
    <SalutationName
      v-model:salutation.capitalize="form.salutation"
      v-model:name.capitalize="form.name"
    ></SalutationName>
    <BaseInput @blur="email = 'blurrr@its.cold'" class="thicc" type="email" v-model="email" label="Email:" />
  </div>
</template>

<script>
import { reactive, ref } from "vue";
import SalutationName from "./components/SalutationName.vue";
import BaseInput from "./components/BaseInput.vue";

export default {
  name: "App",
  components: {
    SalutationName,
    BaseInput,
  },
  setup() {
    const form = reactive({
      salutation: "",
      name: "",
    });

    const email = ref("");

    return {
      form,
      email,
    };
  },
};
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
</style>
