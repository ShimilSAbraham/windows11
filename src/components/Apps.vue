<template>
    <div class="apps">
            <div class="appsContainer" @click="shootThat(1)"> <img src="../assets/svg/Windows_11_logo.svg" alt="windows Logo" /> </div>           
            <transition name="pop">
                <StartMenu v-if="value === 1" />
            </transition>

            <div class="appsContainer" @click="shootThat(2)"> <img class="searchIcon" src="../assets/svg/search.svg" alt="Search"/> </div>
            <transition name="pop">
                <SearchMenu v-if="value === 2" />
            </transition>

            <div class="appsContainer" @click="shootThat(3)"> <img src="../assets/svg/multi_task.svg" alt="Multi Task"/> </div>
            <transition name="pop">
                <ChangeMode v-if="value === 3" />
            </transition>

            <div class="appsContainer" @click="shootThat(4)"> <img class="widgetIcon" src="../assets/svg/widget.svg" alt="Widget"/> </div>
            <transition name="left-slide">
                <Widget v-if="value === 4" :time="time" :day="day"/>
            </transition>

            <div class="appsContainer" @click="shootThat(5)"> <img src="../assets/svg/Windows_Explorer_Icon.svg" alt="File Explorer"/> </div>
            <transition name="pop">
                <FileExplorer v-if="value === 5" />
            </transition>

            <div class="appsContainer" @click="shootThat(6)"> <img class="mozilla" src="../assets/svg/Firefox.svg" alt="Mozilla Firefox"/> </div>
            <transition name="pop">
                <Firefox v-if="value === 6" />
            </transition>

            <div class="appsContainer" @click="shootThat(7)"> <img src="../assets/svg/Microsoft_Store.svg" alt="Microsoft_Store"/> </div>
            <transition name="pop">
                <AppStore v-if="value === 7" @close="closeThis" />
            </transition>

            <div class="appsContainer" @click="shootThat(8)"> <img class="settingsIcon" src="../assets/svg/settings.svg" alt="Settings"/> </div>
            <transition name="pop">
                <Settings v-if="value === 8" />
            </transition>
    </div>
</template>

<script>
import StartMenu from './Apps/StartMenu.vue'
import SearchMenu from './Apps/SearchMenu.vue'
import ChangeMode from './Apps/ChangeMode.vue'
import Widget from './Apps/Widget.vue'
import FileExplorer from './Apps/FileExplorer.vue'
import Firefox from './Apps/Firefox.vue'
import Settings from './Apps/Settings.vue'
import AppStore from './Apps/AppStore.vue'

    export default {
        name: 'Apps',
        props: ['time','day'],
        components: {
            StartMenu, SearchMenu, ChangeMode, Widget, FileExplorer, Firefox, AppStore, Settings
        },
        mounted(){
        },
        data(){
            return{
                value: 0,
            }
        },
        methods: {
            shootThat(id){
                if(this.value === id)
                    this.value = 0
                else
                    this.value=id
            },
            closeThis(){
                this.value=0
            },
        }
    }
</script>

<style scoped>
    /* app container inside taskbar */
    .apps {
    --apps-hover: #5d637465;
    --main-bg: #171617fb;
    --bg: #201f20;
    --fg: #d6d6d6;
    --icon-color: white;

    --border: 2px solid rgba(49, 46, 46, 0.404);

    width: 22vw;
    height: 100%;
    display: flex;
    justify-content: space-evenly;
    align-items: center;

    }
    /* apps inside app container */
    .apps .appsContainer {
    width: 35px;
    height: 35px;
    border-radius: 3px;
    display: flex;
    justify-content: center;
    align-items: center;
    cursor: pointer;
    transition: background-color 0.8s ease;
    }
    .apps .appsContainer:hover {
    background-color: var(--apps-hover);
    }
    /* app icons */
    .apps .appsContainer img {
    width: 22px;
    transition: transform 0.2s ease;
    }
    .apps .appsContainer .settingsIcon {
    transition: transform 0.5s ease;
    }
    .apps .appsContainer img:active {
    transform: scale(0.8);
    }
    .apps .appsContainer .searchIcon:active {
    transform: scale(0.8) rotate(40deg);
    }
    .apps .appsContainer .widgetIcon:active {
    transform: translateX(5px);
    }
    .apps .appsContainer .mozilla:active {
    transform: rotate(360deg);
    }
    .apps .appsContainer .settingsIcon:active {
    transform: rotate(180deg);
    }


</style>