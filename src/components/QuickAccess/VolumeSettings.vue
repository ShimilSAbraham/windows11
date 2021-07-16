<template>
  <div class="volumeSettings">
    <div class="volumeSettingsTitle">Speaker / Headphone</div>
    <div class="volumeControl">
      <i class="far fa-volume"></i>
      <div class="volumeSlider">
        <input
          v-model="percent"
          type="range"
          class="volumeSliderInput"
          min="0"
          max="100"
        />
        <div
          class="volumeSliderProgress"
          :style="{ width: percent + '%' }"
        ></div>
      </div>
      <div class="volumeValue">{{ percent }}</div>
    </div>
    <div class="volumeBottom">
      <i class="fas fa-cog"></i>
    </div>
  </div>
</template>

<script>
export default {
    name: 'VolumeSettings',
    data() {
    return {
      percent: 40,
    };
  },
}
</script>

<style scoped>
.volumeSettings {
  position: absolute;
  bottom: 101px;
  right: 5px;
  width: 385px;
  height: 120px;
  border-radius: 10px 10px 0 0;

  font-family: "Calibri", sans-serif;
  background-color: #171617f0;
  border-bottom: 3px solid #5f5f5f99;
  display: flex;
  flex-direction: column;
  align-items: center;
  justify-content: space-evenly;
}

.volumeSettings .volumeSettingsTitle {
  align-self: flex-start;
  margin-left: 1rem;
  font-size: 1.2rem;
  font-weight: 400;
  color: #CFCFCF;
}

.volumeSettings .volumeControl {
  display: flex;
  flex-direction: row;
  align-items: center;
  justify-content: space-between;
  width: 90%;
  height: 40%;
}

.volumeSettings .volumeControl > i {
  color: #CFCFCF;
  font-size: 1.5rem;
}

.volumeSettings .volumeControl .volumeSliderInput {
  width: 100%;
}

.volumeSettings .volumeControl .volumeValue {
  font-size: 1.4rem;
  color: #CFCFCF;
  width: 35px;
}

.volumeSettings .volumeSlider {
  height: 5px;
  width: 80%;
  background: white;
  border-radius: 5px;
  margin: 0 15px;
  background: #888888;

  position: relative;
  display: flex;
  align-items: center;
  justify-content: center;
}
.volumeSettings .volumeSliderInput {
  -webkit-appearance: none;
  background: transparent;
  outline: none;
  border: none;
  height: 100%;
  width: 100%;
  border-radius: 5px;
  z-index: 2;
}
.volumeSettings .volumeSliderInput::-webkit-slider-thumb {
  -webkit-appearance: none;
  width: 10px;
  height: 10px;
  border-radius: 50%;
  cursor: pointer;
  transition: box-shadow 0.5s;
  background: #198f85;
  box-shadow: 0 0 0 6px #282828;
}
.volumeSettings .volumeSliderInput:active::-webkit-slider-thumb {
  box-shadow: 0 0 0 6px #282828, 0 0 0 15px #198f8570;
}
.volumeSettings .volumeSliderInput::-moz-range-thumb {
  -webkit-appearance: none;
  width: 10px;
  height: 10px;
  border-radius: 50%;
  cursor: pointer;
  transition: box-shadow 0.5s;
  background: #198f85;
  box-shadow: 0 0 0 6px #282828;
}
.volumeSettings .volumeSliderInput:active::-moz-range-thumb {
  box-shadow: 0 0 0 6px #282828, 0 0 0 15px #198f8570;
}
.volumeSettings .volumeSliderProgress {
  position: absolute;
  left: 0;
  height: 100%;
  border-radius: 5px;
  background: #198f85;
  z-index: 1;
}

.volumeSettings .volumeBottom {
  position: absolute;
  bottom: -53px;
  height: 50px;
  width: 100%;
  border-radius: 0 0 10px 10px;
  background: #201f20;

  display: flex;
  padding-right: 20px;
  justify-content: flex-end;
  align-items: center;
}
.volumeSettings .volumeBottom > i {
  color: #CFCFCFa8;
  cursor: pointer;
  font-size: 1.2rem;
  transition: color 0.2s;
}
.volumeSettings .volumeBottom > i:hover {
  color: #CFCFCF;
  transform: rotate(180deg);
}
</style>
