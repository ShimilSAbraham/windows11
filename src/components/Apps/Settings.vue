<template>
  <div class="settings">
      <h1>Coming Soon...</h1>
  </div>
</template>

<script>
export default {
    name: 'Settings'
}
</script>

<style scoped>
    .settings{
        position: absolute;
        bottom: 55px;
        width: 60vw;
        border-radius: 10px;
        height: 85vh;
        background: var(--main-bg);
        background-image: url('../../assets/svg/settings.svg');
        background-repeat: no-repeat;
        background-position: center;
        
        border: var(--border);
        z-index: -5;
        backdrop-filter: blur( 12px );
        -webkit-backdrop-filter: blur( 12px );
    }
    .settings h1{
        position: absolute;
        bottom: 30%;
        left: 50%;
        transform: translateX(-50%);
        color: var(--fg);
    }
</style>