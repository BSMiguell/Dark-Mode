<template>
  <header>
    <h1>{{ mode }} Mode</h1>
    <ToggleView :mode="mode" @toggle="$emit('toggle')" />

    <nav>
      <div class="nav-link">Home</div>
      <div class="nav-link">About</div>
      <div class="nav-link">Portfolio</div>
      <div class="nav-link">Contact</div>
    </nav>
  </header>
</template>

<script>
import ToggleView from "@/components/ToggleView";

export default {
  props: ["mode"],

  components: {
    ToggleView,
  },
};
</script>

<style>
header {
  display: flex;
  justify-content: space-between;
  align-items: center;
  padding: 0px 25px;
  height: 60px;
  background: #c3c3c3;
  transition: background 0.3s ease-in-out;
}
.dark header {
  background: #15202b;
}
.dark header nav .nav-link:hover {
  background: #101520;
}
header h1 {
  font-size: 32px;
  text-transform: uppercase;
  font-weight: 900;
}
header nav {
  display: flex;
  height: 60px;
}
header nav .nav-link {
  display: flex;
  align-items: center;
  padding: 0px 15px;
}
header nav .nav-link:hover {
  background: #b0b0b0;
}
</style>
