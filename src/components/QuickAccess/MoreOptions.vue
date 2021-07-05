<template>
    <div class="moreOptions">
        <!-- <div class="hiddenIcon">
            <img src="vue.svg" alt="" />
        </div>
        <div class="hiddenIcon">
            <img src="react.svg" alt="" />
        </div>
        <div class="hiddenIcon">
            <img src="angularreact.svg" alt="" />
        </div>
        <div class="hiddenIcon">
            <img src="javascript.svg" alt="" />
        </div>
        <div class="hiddenIcon"></div>
        <div class="hiddenIcon"></div> -->
  </div>
</template>

<script>
export default {
    name: 'MoreOptions',
}
</script>

<style>
    .moreOptions{
        position: absolute;
        top: -16.5vh;
        right: 8.3vw;
        border-radius: 5px;
        width: 180px;
        height: 120px;
        background: var(--main-bg);
        border: var(--border);
        z-index: -5;
    }
</style>