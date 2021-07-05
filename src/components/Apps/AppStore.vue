<template>
  <div class="appStore">
    <AppStoreHeader />
    <AppStoreMenu />
    <AppStoreMain />
  </div>
</template>

<script>
import AppStoreHeader from "../Apps/AppStore/AppStoreHeader.vue";
import AppStoreMenu from "../Apps/AppStore/AppStoreMenu.vue";
import AppStoreMain from "../Apps/AppStore/AppStoreMain.vue";

export default {
  name: "AppStore",
  components: {
    AppStoreHeader,
    AppStoreMenu,
    AppStoreMain,
  },
};
</script>

<style scoped>
.appStore {
  /* variables */
  --inputs: #111111;
  --icons: #198f85;
  --btn-hover: #72727259;
  --close-btn-hover: #c21212a4;

  --search-shadow: 0px 0px 4px 1px #00000099;
  --icons-active: #e4e4e4;
  /* variables */

  width: 70vw;
  height: 85vh;
  border-radius: 15px;
  background: #171617e0;
  position: absolute;
  top: -89vh;

  border: var(--border);
  z-index: -5;
  backdrop-filter: blur( 12px );
  -webkit-backdrop-filter: blur( 12px );

}
</style>
