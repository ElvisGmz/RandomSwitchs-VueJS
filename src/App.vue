<template>
  <h1>Random Switchs</h1>
  <SwitchCard />
</template>

<script>
import SwitchCard from "./components/SwitchCard.vue";

export default {
  name: "App",
  components: {
    SwitchCard,
  },
};
</script>

<style>
body {
  background-color: #ff3cac;
  background-image: linear-gradient(
    225deg,
    #ff3cac 0%,
    #784ba0 50%,
    #2b86c5 100%
  );

  color: #21212c;
  font-family: Verdana, Geneva, Tahoma, sans-serif;
  min-height: 100vh;
  margin: 0;
  box-sizing: border-box;
  padding: 1rem;
  display: flex;
  justify-content: center;
  align-items: center;
}

h1 {
  text-align: center;
  font-size: 24px;
  color: #fff;
}
</style>
