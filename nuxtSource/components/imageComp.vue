<template>
    <div class="image-component">
      <!-- <div class="flex m-auto"> -->
        <h4>v-img tag test</h4>
        <v-img
            alt="dynamic img"
            lazy-src="https://picsum.photos/id/11/10/6"
            max-height="150"
            max-width="250"
            src="https://picsum.photos/id/11/500/300"
        ></v-img>
        <h4>dynamic image test</h4>
        <img
            alt="dynamic img"
            src="https://picsum.photos/id/11/500/300"
        >
        <h4>static image test</h4>
        <img
            class="VuetifyLogo"
            alt="Vuetify Logo"
            src="/vuetify-logo.svg"
        >
      <!-- </div> -->
      <!-- <div class="flex m-auto"> -->
        <h4>dynamic image test</h4>
        <img
            alt="dynamic img"
            src="https://picsum.photos/id/11/500/300"
        >
        <h4>static image test</h4>
        <img
            class="VuetifyLogo"
            alt="Vuetify Logo"
            src="/vuetify-logo.svg"
        >
      <!-- </div> -->
    </div>
</template>

<style>
.VuetifyLogo {
  height: 180px;
  width: 180px;
  transform: rotateY(560deg);
  animation: turn 3.5s ease-out forwards 1s;
}

@keyframes turn {
  100% {
    transform: rotateY(0deg);
  }
}
</style>
