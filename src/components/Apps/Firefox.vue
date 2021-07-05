<template>
  <div class="firefox">
      <h1>Coming Soon...</h1>
  </div>
</template>

<script>
export default {
    name: 'Firefox'
}
</script>

<style scoped>
    .firefox{
        position: absolute;
        bottom: 55px;
        width: 60vw;
        border-radius: 10px;
        height: 85vh;
        background: var(--main-bg);
        background-image: url('../../assets/svg/Firefox.svg');
        background-repeat: no-repeat;
        background-position: center;
        background-size: 20%;

        border: var(--border);
        z-index: -5;
        backdrop-filter: blur( 12px );
        -webkit-backdrop-filter: blur( 12px );
    }
    .firefox h1{
        position: absolute;
        bottom: 25%;
        left: 50%;
        transform: translateX(-50%);
        color: var(--fg);
    }
</style>