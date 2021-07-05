<template>
  <div class="fileExplorer">
      <h1>Coming Soon...</h1>
  </div>
</template>

<script>
export default {
    name: 'FileExplorer'
}
</script>

<style scoped>
    .fileExplorer{
        position: absolute;
        bottom: 55px;
        width: 60vw;
        border-radius: 10px;
        height: 85vh;
        background: var(--main-bg);
        background-image: url('../../assets/svg/Windows_Explorer_Icon.svg');
        background-repeat: no-repeat;
        background-position: center;

        border: var(--border);
        z-index: -5;
        backdrop-filter: blur( 12px );
        -webkit-backdrop-filter: blur( 12px );
    }
    .fileExplorer h1{
        position: absolute;
        bottom: 30%;
        left: 50%;
        transform: translateX(-50%);
        color: var(--fg);
    }
</style>