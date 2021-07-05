<template>
  <div class="trendingApps">
    <div class="title">
      <h3>Trending apps</h3>
      <button>See all</button>
    </div>
    <div class="apps">
      <div class="item"></div>
      <div class="item"></div>
      <div class="item"></div>
      <div class="item"></div>
      <div class="item"></div>
      <div class="item"></div>
    </div>
  </div>
</template>

<script>
export default {
  name: "TrendingApps",
};
</script>

<style scoped>
.trendingApps {
  height: 35%;
  width: 98%;
  border-radius: 5px;
  box-sizing: border-box;

  display: flex;
  flex-direction: column;
  align-items: center;
  justify-content: space-around;
}
.trendingApps .title {
  height: 20%;
  width: 98%;
  margin: 10px;
  display: flex;
  align-items: center;
  justify-content: space-between;
}
.trendingApps .title h3 {
  display: flex;
  justify-content: center;
  align-items: center;
  color: var(--fg);
  -webkit-user-select: none;
  -ms-user-select: none;
  user-select: none;
}
.trendingApps .title button {
  height: 20px;
  width: 60px;
  font-size: 0.85rem;
  font-family: "arial";
  font-weight: bold;
  border-radius: 3px;
  color: var(--fg);
  background: var(--bg);
  box-shadow: 1px 1px 2px #00000079, -1px -1px 2px #ffffff19;
  border: none;
  outline: none;
}
.trendingApps .title button:active {
  box-shadow: inset 1px 1px 2px #00000079, inset -1px -1px 2px #ffffff19;
  transform: translateY(-2px);
  font-size: 0.82rem;
}
.trendingApps .title button:hover {
  background: rgba(17, 17, 17, 0.5);
}
.trendingApps .apps {
  height: 70%;
  width: 100%;
  display: flex;
  align-items: center;
  justify-content: space-around;
}

.trendingApps .apps .item {
  background: rgba(10, 10, 10, 0.623);
  height: 100%;
  width: 16%;
  border-radius: 5px;
  transition: transform 0.5s, background-color 0.5s;

  /* box-sizing: border-box; */
}
.trendingApps .apps .item:hover {
  transform: scale(1.02);
  background-color: #111111;
}
</style>
