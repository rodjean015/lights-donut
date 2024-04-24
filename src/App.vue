<template>

  <div class=" bg-white h-screen">
    <Navbar />
    <RouterView />
  </div>

</template>

<script>
import Navbar from "./components/Navbar.vue";

export default {
  name: "App",
  components: {
    Navbar,
  },
};

</script>