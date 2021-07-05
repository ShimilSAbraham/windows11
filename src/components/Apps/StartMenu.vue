<template>
  <div class="startMenu">
      <h1>Coming Soon...</h1>
  </div>
</template>

<script>
export default {
    name: 'StartMenu'
}
</script>

<style scoped>
    .startMenu{
        position: absolute;
        top: -81vh;
        width: 36vw;
        border-radius: 10px;
        height: 80vh;
        background: var(--main-bg);
        background-image: url('../../assets/svg/Windows_11_logo.svg');
        background-repeat: no-repeat;
        background-position: center;

        border: var(--border);
        z-index: -5;
        backdrop-filter: blur( 12px );
        -webkit-backdrop-filter: blur( 12px );
    }
    .startMenu h1{
        position: absolute;
        bottom: 30%;
        left: 50%;
        transform: translateX(-50%);
        color: var(--fg);
    }
</style>