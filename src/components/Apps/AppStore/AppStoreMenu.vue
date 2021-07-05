<template>
  <div class="appStoreMenu">
    <div class="menuTop">
      <MenuItem
        v-for="item in itemsTop"
        :key="item"
        :i="item.icon"
        :title="item.name"
        @click="checkActive(item.num)"
        :class="activeMenuItem === item.num && 'menuItemActive'"
      />
    </div>
    <div class="menuBottom">
      <MenuItem
        v-for="item in itemsBottom"
        :key="item"
        :i="item.icon"
        :title="item.name"
        @click="checkActive(item.num)"
        :class="activeMenuItem === item.num && 'menuItemActive'"
      />
    </div>
  </div>
</template>

<script>
import MenuItem from "./AppStoreMenu/MenuItem.vue";
export default {
  name: "AppStoreMenu",
  components: {
    MenuItem,
  },
  data() {
    return {
      itemsTop: [
        { name: "Home", icon: "far fa-home", num: 1 },
        { name: "Apps", icon: "far fa-cubes", num: 2 },
        { name: "Gaming", icon: "far fa-gamepad", num: 3 },
        { name: "Movies", icon: "far fa-film", num: 4 },
      ],
      itemsBottom: [
        { name: "Library", icon: "far fa-books", num: 5 },
        { name: "Settings", icon: "far fa-cog", num: 6 },
      ],
      activeMenuItem: 1,
    };
  },
  methods: {
    checkActive(num) {
      this.activeMenuItem = num;
      console.log(this.activeMenuItem);
    },
  },
};
</script>

<style scoped>
.appStoreMenu {
  position: absolute;
  top: 8%;
  width: 7%;
  height: 90%;

  display: flex;
  flex-direction: column;
  align-items: center;
  justify-content: space-around;
}

.menuTop,
.menuBottom {
  width: 90%;
  display: flex;
  flex-direction: column;
  justify-content: space-evenly;
  align-items: center;
}
.menuTop {
  height: 45%;
  margin-top: -80%;
}
.menuBottom {
  height: 25%;
  margin-bottom: -50%;
  transform: translateY(20%);
}
</style>
