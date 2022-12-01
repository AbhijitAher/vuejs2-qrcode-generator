<template>
  <div>
    <h2>VueJS QRCode Generator</h2>
    <br />
    <h4>Enter Your Text below to generate the QRCode</h4>

    <textarea
      class="input"
      type="text"
      placeholder="Text"
      @input="setQRString"
    />

    <div>
      <qrcode :value="QRString" :options="{ width: 300 }"></qrcode>
    </div>
  </div>
</template>

<script>
import VueQrcode from "@chenfengyuan/vue-qrcode";
// https://github.com/soldair/node-qrcode#qr-code-options
// https://github.com/fengyuanchen/vue-qrcode/tree/v1

import Vue from "vue";

Vue.component(VueQrcode.name, VueQrcode);

export default {
  name: "QRCodeComponent",

  props: {
    msg: String,
  },
  data() {
    return {
      QRString: "",
    };
  },

  methods: {
    setQRString(e) {
      let value = e.target.value;
      this.QRString = value;
    },
  },
};
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
.input {
  margin-top: 20px;
  padding: 10px;
  border-radius: 5px;
  height: 100px;
  width: 300px;
  border: 2px solid rgb(189, 66, 189);
}
</style>
