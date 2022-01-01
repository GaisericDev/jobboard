<template>
  <div class="app">
    <p>Hello {{ name }} - {{ age }}</p>
    <button @click="changeName('Gankerjack')">change name</button>
    <button @click="changeAge(28)">change age</button>
  </div>
</template>

<script lang="ts">
import { defineComponent } from "vue";

export default defineComponent({
  name: "App",
  components: {},
  data() {
    return {
      name: "Gaiseric",
      age: 27 as number | string,
    };
  },
  methods: {
    changeName(name: string): string {
      this.name = name;
      return name;
    },
    changeAge(age: number | string): string | number {
      this.age = age;
      return age;
    },
  },
});
</script>

<style>
</style>
