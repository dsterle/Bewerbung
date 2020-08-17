<template>
  <div id="app">
    <b-container>
      <b-row>
        <b-col>
          <h1>Willkommen auf meiner Bewerbungsseite!</h1>
        </b-col>
      </b-row>
      <b-row>
        <b-col class="animated fadeInLeft">
          <h2>Mein Name ist Dennis Sterle!</h2>
          <b-container class="basicInformation">
            <b-row v-for="item in basicInformation" :key="item" class="text-start">
              <b-col cols="5">
                {{item[0]}}
              </b-col>
              <b-col class="text-left">
                {{item[1]}}
              </b-col>
            </b-row>
          </b-container>
        </b-col>
        <b-col>
          <b-img :src="image_ds" fluid rounded="circle" alt="Dennis Sterle" id="image_ds" class="animated bounceIn"></b-img>
        </b-col>
      </b-row>
    </b-container>
  </div>
</template>

<script>
//import Home from './components/Home.vue'

export default {
  name: 'App',
  components: {
  },
  data() {
    return {
      image_ds: require("../src/assets/images/picture_of_me.png"),
      basicInformation: [
        ["Mobil", "01717515637"],
        ["Email", "dennissterle@yahoo.de"],
        ["Anschrift", "Am Sandberg 28\n51643 Gummersbach"]
      ]
    }
  }
}
</script>

<style lang="scss">
@import url("https://cdnjs.cloudflare.com/ajax/libs/meyer-reset/2.0/reset.min.css");
@import url("https://cdnjs.cloudflare.com/ajax/libs/font-awesome/5.11.2/css/all.css");
@import "./src/assets/scss/site.scss";

h1 {
  font-size: $font-size-XXXL;
  margin: $abstand-XXL $abstand-XXXXL;
}

h2 {
  font-size: $font-size-L;
}

#image_ds {
  height: 500px;
  width: 500px;
  animation-delay: 800ms;
}

.basicInformation {
  margin-top: $abstand-L;
}
</style>
