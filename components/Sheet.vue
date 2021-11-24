<template>
  <div class="main">
    <div class="ripple-main">
      <div class="ripple-box">
        <img id="turkey" src="@/assets/images/turkey.png">
        <h1>Thank you, {{ name }}</h1>
        <p>
          <slot name="message" />
        </p>
        <p><b>- Caine & Rebekah</b></p>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  props: {
    name: {
      type: String,
      default: ''
    }
  }
};
</script>

<style scoped>
.ripple-main {
  filter: drop-shadow(-1px 6px 3px rgba(0, 0, 0, 0.5));
  padding-left: 5vw;
  padding-right: 5vw;
  display: grid;
  grid-template-rows: min-content;
  align-content: center;
  height: 100vh;
  box-sizing: border-box;
}
.ripple-main .ripple-box {
  position: relative;
  height: auto;
  overflow: hidden;
  margin: auto;
  max-width: 70ch;
  padding-top: 10ch;
  padding-bottom: 10ch;
  padding-left: 10ch;
  padding-right: 10ch;
  background-image: url("data:image/svg+xml,%3Csvg%20xmlns%3D%22http%3A%2F%2Fwww.w3.org%2F2000%2Fsvg%22%3E%0A%20%20%20%20%3Cdefs%3E%0A%20%20%20%20%20%20%20%20%3Cfilter%20id%3D%22roughpaper%22%3E%0A%20%20%20%20%20%20%20%20%20%20%20%20%3CfeTurbulence%20type%3D%22fractalNoise%22%20baseFrequency%3D%220.015%22%20numOctaves%3D%225%22%20result%3D%22noise%22%20%2F%3E%0A%20%20%20%20%20%20%20%20%20%20%20%20%3CfeDiffuseLighting%20lighting-color%3D%22%23ecd7bb%22%20diffuseConstant%3D%221%22%20surfaceScale%3D%222%22%20result%3D%22diffLight%22%3E%0A%20%20%20%20%20%20%20%20%20%20%20%20%20%20%20%20%3CfeDistantLight%20azimuth%3D%2245%22%20elevation%3D%2235%22%20%2F%3E%0A%20%20%20%20%20%20%20%20%20%20%20%20%3C%2FfeDiffuseLighting%3E%0A%20%20%20%20%20%20%20%20%3C%2Ffilter%3E%0A%20%20%20%20%3C%2Fdefs%3E%0A%0A%20%20%20%20%3Crect%20filter%3D%22url(%23roughpaper)%22%20width%3D%22100%25%22%20height%3D%22100%25%22%20fill%3D%22%23ecd7bb%22%20%2F%3E%0A%3C%2Fsvg%3E");
  clip-path: polygon(
    1% 2%,
    3.5% 0.1%,
    8.9% 2.7%,
    16.2% 1.2%,
    19.7% 0.8%,
    24.7% 2%,
    31.2% 0%,
    35.9% 2.3%,
    40.6% 0.5%,
    47.1% 1.8%,
    49.9% 1%,
    53.8% 2.5%,
    62.2% 0.4%,
    67.3% 1.2%,
    70.3% 0.3%,
    75.8% 1.4%,
    78.5% 1.7%,
    84% 2.6%,
    91.1% 0.5%,
    93.6% 2.4%,
    97.3% 0.3%,
    98.9% 6%,
    98.1% 11.4%,
    98.6% 15.5%,
    97.3% 17.8%,
    97.7% 27.4%,
    98.3% 28.5%,
    99.7% 34.1%,
    98.8% 41.9%,
    98.3% 45.7%,
    98.4% 50.9%,
    98.7% 57.4%,
    99.6% 60.4%,
    99.4% 66.6%,
    99.2% 69.5%,
    97.4% 77.1%,
    98.1% 82.3%,
    99.9% 83.5%,
    98.2% 91.5%,
    99.3% 95.3%,
    98% 98.6%,
    93.6% 97.4%,
    90.3% 98.3%,
    86.8% 98.3%,
    78.6% 98.5%,
    76.4% 99.2%,
    69.7% 99.8%,
    64.2% 99.3%,
    61.8% 99.2%,
    57.2% 98.1%,
    48.7% 98.3%,
    46.8% 99%,
    39.6% 98.9%,
    33.8% 97.3%,
    28.2% 99.4%,
    27% 98.3%,
    22.1% 98.6%,
    13.1% 97.1%,
    8.7% 99.3%,
    2.7% 97.4%,
    2% 98.2%,
    2.1% 94.3%,
    0.7% 90.5%,
    0.9% 86.3%,
    2.2% 78.2%,
    0.4% 76.7%,
    1.2% 72.1%,
    2% 64%,
    1.4% 59.8%,
    0.4% 57.3%,
    0.3% 49.1%,
    2.9% 44.7%,
    1.9% 41.3%,
    0.8% 35.7%,
    2.9% 31.3%,
    0.8% 24.9%,
    2.7% 20.5%,
    0.8% 17.4%,
    2.5% 8.6%,
    1.1% 5.5%
  );
}

#turkey {
  position: absolute;
  top: 7.5%;
  right: 7.5%;
  width: 15%;
  animation-duration: 5s;
  animation-name: wiggle;
  animation-iteration-count: infinite;
  -webkit-filter: drop-shadow(-1px 6px 3px rgba(0, 0, 0, 0.5));
  filter: drop-shadow(-1px 6px 3px rgba(0, 0, 0, 0.5));
}

@keyframes wiggle {
  0% {
    transform: rotate(15deg);
  }
  50% {
    transform: rotate(30deg);
  }
  100% {
    transform: rotate(15deg);
  }
}
</style>
