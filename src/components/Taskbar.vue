<template>

    <div class="taskbar">
        <Apps :time="time" :day="day" />
        <QuickAccess :time="time" :date="date" :day="day" />
    </div>
    
</template>

<script>
import Apps from "./Apps.vue"
import QuickAccess from "./QuickAccess.vue"

export default {
    name: 'Taskbar',
    props: ['time','date','day'],
    components: {
        Apps,
        QuickAccess,
    },
}

</script>

<style scoped>
    /* taskbar div */
    .taskbar {
    --taskbar-bg: rgba(18, 24, 39, 0.8);

    display: flex;
    justify-content: center;
    position: relative;
    bottom: 0;
    width: 100vw;
    height: 45px;
    
    background-color: var(--taskbar-bg);
    backdrop-filter: blur( 6.0px );
    -webkit-backdrop-filter: blur( 6.0px );
    -moz-backdrop-filter: blur( 6.0px );

    z-index: 100;
    }
</style>