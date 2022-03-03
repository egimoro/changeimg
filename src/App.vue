<script>
import image1 from "./assets/ichigo.jpeg";
import image2 from "./assets/rukia.jpeg";
import image3 from "./assets/ulquiorra.jpeg";
import image4 from "./assets/getsugatenshou.jpeg";

export default {
  data() {
    return {
      image1: image1,
      image2: image2,
      image3: image3,
      image4: image4,
      showImg: 1,
    };
  },

  methods: {
    changeimg() {
      if (this.showImg == 1) {
        this.showImg = 2;
      } else if (this.showImg == 2) {
        this.showImg = 3;
      } else if (this.showImg == 3) {
        this.showImg = 4;
      } else {
        this.showImg = 1;
      }
    },
  },
};
</script>

<template>
  <div>
    <div v-if="showImg == 1">
      <img class="borderhead" :src="image1" alt="ichigo" />
    </div>
    <div v-else-if="showImg == 2">
      <img class="borderhead" :src="image2" alt="rukia" />
    </div>
    <div v-else-if="showImg == 3">
      <img class="borderhead" :src="image3" alt="ulquiorra" />
    </div>
    <div v-else>
      <img class="borderhead" :src="image4" alt="getsugatenshou" />
    </div>
    <button @click="changeimg">Change Image</button>
  </div>
</template>

<style>
img {
  width: 600px;
  height: 500px;
}
.borderhead {
  border: 2px solid;
  border-color: blue;
  border-radius: 5px;
}
button {
  border: 2px solid black;
  border-radius: 8px;
  padding: 5px;
  font-size: 20px;
  font-family: fantasy;
  background-color: aqua;
}
body {
  background-color: rgba(229, 255, 204, 0.5);
  background-image: url("./assets/urahara.jpeg");
  background-repeat: no-repeat;
  background-position: 80% 80%;
}
</style>
