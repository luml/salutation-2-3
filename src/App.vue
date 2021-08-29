<template>
  <div id="app">
    <SalutationName
      v-model:salutation.capitalize="form.salutation"
      v-model:name.capitalize="form.name"
    ></SalutationName>
  </div>
</template>

<script>
import { reactive } from "vue";
import SalutationName from "./components/SalutationName.vue";

export default {
  name: "App",
  components: {
    SalutationName,
  },
  setup() {
    const form = reactive({
      salutation: "",
      name: "",
    });

    return {
      form,
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
