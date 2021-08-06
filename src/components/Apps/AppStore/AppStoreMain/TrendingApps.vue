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
  height: 40%;
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

.trendingApps .apps .item:nth-child(1) {
  --appName: 'Telegram';
  --desc: 'Social';
  background-image: url('https://upload.wikimedia.org/wikipedia/commons/thumb/8/82/Telegram_logo.svg/1024px-Telegram_logo.svg.png');
}
.trendingApps .apps .item:nth-child(2) {
  --appName: 'Whatsapp';
  --desc: 'Social';
  background-image: url('https://upload.wikimedia.org/wikipedia/commons/thumb/6/6b/WhatsApp.svg/1200px-WhatsApp.svg.png');
}
.trendingApps .apps .item:nth-child(3) {
  --appName: 'Visual Studio Code';
  --desc: 'Developer Tools';
  background-image: url('https://dashboard.snapcraft.io/site_media/appmedia/2019/05/code_ozwVHSV.png');
}
.trendingApps .apps .item:nth-child(4) {
  --appName: 'Adobe Lightroom';
  --desc: 'Photo & Video';
  background-image: url('https://upload.wikimedia.org/wikipedia/commons/thumb/b/b6/Adobe_Photoshop_Lightroom_CC_logo.svg/1200px-Adobe_Photoshop_Lightroom_CC_logo.svg.png');
}
.trendingApps .apps .item:nth-child(5) {
  --appName: 'Figma';
  --desc: 'Productivity';
  background-image: url('https://cdn.sanity.io/images/599r6htc/production/46a76c802176eb17b04e12108de7e7e0f3736dc6-1024x1024.png?w=670&h=670&q=75&fit=max&auto=format');
}
.trendingApps .apps .item:nth-child(6) {
  --appName: 'Github Desktop';
  --desc: 'Productivity';
  background-image: url('https://user-images.githubusercontent.com/1784648/97818784-c4fc1080-1ca4-11eb-8681-56ec3fa21756.png');
}

.trendingApps .apps .item {
  background: rgba(10, 10, 10, 0.623);
  background-size: 45%;
  background-repeat: no-repeat;
  background-position: center 20%;

  position: relative;
  height: 100%;
  width: 16%;
  border-radius: 5px;
  cursor: pointer;
  transition: all 0.5s;

  /* box-sizing: border-box; */
}
.trendingApps .apps .item::before {
    position: absolute;
    content: var(--appName);
    font-size: 0.9rem;
    color: #d6d6d6;
    font-weight: 600;
    top: 65%;
    left: 50%;
    transform: translateX(-50%);
}
.trendingApps .apps .item::before {
    position: absolute;
    content: var(--appName);
    font-size: 0.9rem;
    color: #d6d6d6;
    font-weight: 600;
    top: 65%;
    left: 50%;
    transform: translateX(-50%);
}

.apps .item::after {
    position: absolute;
    content: var(--desc);
    font-size: 0.7rem;
    color: #d6d6d699;
    font-weight: 500;
    top: 78%;
    left: 50%;
    transform: translateX(-50%);
}

.trendingApps .apps .item:hover {
  transform: scale(1.02);
  background-color: #111111;
}
</style>
