<template>
  <div class="app" :class="mode">
    <HeaderView :mode="mode" @toggle="toggle" />
    <ContentView :mode="mode" />
  </div>
</template>

<script>
import HeaderView from "@/components/HeaderView";
import ContentView from "@/components/ContentView";

export default {
  name: "App",
  data() {
    return {
      mode: "light",
    };
  },
  components: {
    HeaderView,
    ContentView,
  },
  created() {
    window.addEventListener("keyup", this.keyPress);
  },
  methods: {
    keyPress(e) {
      if (e.key === "t") {
        this.toggle();
      }
    },
    toggle() {
      if (this.mode === "dark") {
        this.mode = "light";
      } else {
        this.mode = "dark";
      }
    },
  },
};
</script>

<style>
* {
  margin: 0;
  padding: 0;
  box-sizing: border-box;
  font-family: "Roboto", sans-serif;
}

.app {
  width: 100vw;
  min-height: 100vh;
  background: #f3f3f3;
  color: #15202b;
  transition: background 0.3s ease-in-out;
}

.dark {
  background: #192734;
  color: #f3f3f3;
}
</style>
