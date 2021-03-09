<template>
  <main class="card">
    <div class="switch" v-on:click="changeRandom()" v-bind:class="{on: stateSw1}" />
    <div class="switch" v-on:click="changeRandom()" v-bind:class="{on: stateSw2}" />
    <div class="switch" v-on:click="changeRandom()" v-bind:class="{on: stateSw3}" />
    <div class="switch" v-on:click="changeRandom()" v-bind:class="{on: stateSw4}" />
    <div class="switch" v-on:click="changeRandom()" v-bind:class="{on: stateSw5}" />
  </main>
</template>

<script>
export default {
  name: "SwitchCard",

  data() {
    return {
      stateSw1: Math.random() < 0.5,
      stateSw2: Math.random() < 0.5,
      stateSw3: Math.random() < 0.5,
      stateSw4: Math.random() < 0.5,
      stateSw5: Math.random() < 0.5
    }
  },
  methods: {
    changeRandom(){
      this.stateSw1 = Math.random() < 0.5;
      this.stateSw2 = Math.random() < 0.5;
      this.stateSw3 = Math.random() < 0.5;
      this.stateSw4 = Math.random() < 0.5;
      this.stateSw5 = Math.random() < 0.5;
    }
  }
  
};
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
.card {
  background-color: #fff;
  width: 250px;
  min-height: 400px;
  box-sizing: border-box;
  padding: 2.5rem 1rem;
  display: flex;
  justify-content: space-evenly;
  align-items: center;
  flex-flow: column nowrap;
  border-radius: 10px;
}

.switch {
  background-color: #e0e0e0;
  width: 100px;
  height: 35px;
  border-radius: 50px;
  position: relative;
  cursor: pointer;
  margin-bottom: 1rem;
  transition: all 0.4s;
}

.on{
  background-color: #21212c;
}

.switch::after {
  content: "";
  position: absolute;
  width: 35px;
  height: 35px;
  border: 5px crimson solid;
  box-shadow: 0px 0px 15px orangered;
  box-sizing: border-box;
  border-radius: 50%;
  background-color: white;
  transition: all 0.4s;
  cursor: pointer;
  right: 65px;
}

.on::after{
  right: 0;
  border: 5px dodgerblue solid;
  box-shadow: 0px 0px 15px cyan;
}
</style>
