<template>
  <div class="notifications">
    <div class="upperPart"></div>
    <div class="middlePart">
      No new notifications
    </div>
    <div class="bottomPart"></div>
  </div>
</template>

<script>
export default {
  name: "Notifications",
};
</script>

<style scoped>
.notifications {
  position: absolute;
  bottom: 51px;
  right: 5px;

  width: 350px;
  height: 92vh;
  padding: 5px;

  display: flex;
  flex-direction: column;
  align-items: center;
  justify-content: space-between;
}
.notifications .upperPart,.middlePart,.bottomPart {
  font-family: 'Montserrat', sans-serif;
  font-weight: bold;
  color: var(--quick-access-hover);
  height: 30%;
  width: 100%;
  background-color: var(--main-bg);
  border: var(--border);
  border-radius: 6px;

  display: flex;
  align-items: center;
  justify-content: center;
}
.notifications .bottomPart {
  height: 38%;
}
</style>