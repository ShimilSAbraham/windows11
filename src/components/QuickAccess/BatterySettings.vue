<template>
  <div class="batterySettings"></div>
</template>

<script>
export default {
  name: "BatterySettings",
};
</script>

<style scoped>
.batterySettings {
  position: absolute;
  bottom: 51px;
  right: 5px;
  
  width: 350px;
  height: 200px;
  padding: 3px;
  border-radius: 8px;

  background-color: var(--main-bg);
  border: var(--border);

  display: flex;
}
</style>