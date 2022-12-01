<template>
  <div id="app">
    <QRCodeComponent />
  </div>
</template>

<script>
import QRCodeComponent from "./components/QRCode";

export default {
  name: "App",
  components: {
    QRCodeComponent,
  },
};
</script>

<style>
#app {
  font-family: "Avenir", Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
</style>
