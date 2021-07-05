<template>
  <div class="menuItem">
    <div class="menuItemIcon"><i :class="i"></i></div>
    <div class="menuItemText">{{ title }}</div>
  </div>
</template>

<script>
export default {
  name: "MenuItem",
  props: {
    i: String,
    title: String,
  },
};
</script>

<style scoped>
.menuItem {
  font-family: Calibri, sans-serif;
  user-select: none;
  width: 3.5rem;
  height: 3.5rem;
  border-radius: 5px;
  display: flex;
  flex-direction: column;
  justify-content: center;
  cursor: pointer;
  align-items: center;
  color: var(--icons);
  transition: 0.5s;
}
.menuItem:hover {
  background: var(--btn-hover);
}

.menuItemActive {
  position: relative;
  background: var(--icons);
  color: var(--icons-active);
}
.menuItemActive:hover {
  background: var(--icons);
}
.menuItemActive::before {
  content: "";
  position: absolute;
  left: -10%;
  top: 25%;
  border-radius: 5px;
  width: 3px;
  height: 30px;
  background: var(--icons-active);
  transition: 0.3s;
  animation: reveal 0.5s forwards;
}

@keyframes reveal {
  from {
    opacity: 0;
    transform: scale(0);
  }
  to {
    opacity: 1;
    transform: scale(1);
  }
}

.menuItemIcon {
  width: 100%;
  height: 1.5rem;
}
.menuItemIcon i {
  transform: scale(1.3);
}
.menuItemText {
  font-weight: 500;
  font-size: 0.9rem;
}
</style>
