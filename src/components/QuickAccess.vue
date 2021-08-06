<template>
    <div class="quickAccess">
      <div class="access">
          <div class="accessContainer" @click="shootThat(1)"> <i class="fal fa-chevron-up"></i> </div>
            <transition name="popQA">
              <MoreOptions v-if="value === 1" />
            </transition>

          <div class="accessContainer" @click="shootThat(2)"> <img src="../assets/svg/battery-75.svg" alt="battery-75" /> </div>
            <transition name="right-slide">
              <BatterySettings v-if="value === 2" />
            </transition>

          <div class="accessContainer" @click="shootThat(3)"> <i class="fas fa-wifi"></i> </div>
            <transition name="right-slide">
              <NetworkSettings v-if="value === 3" />
            </transition>

          <div class="accessContainer" @click="shootThat(4)"> <i class="fal fa-volume-up"></i> </div>
            <transition name="right-slide">
              <VolumeSettings v-if="value === 4" />
            </transition>

          <div class="QACalendar">
              <div class="QACalItem date">{{date}}</div>
              <div class="QACalItem time">{{time}}</div>
              <div class="QACalItem day">{{day}}</div>
          </div>

          <div class="accessContainer" @click="shootThat(5)"> <i class="fal fa-comment-alt"></i> </div>
            <transition name="right-slide">
              <Notifications v-if="value === 5" />
            </transition>

          <div class="home" @click="refresh"></div>
      </div>

    </div>
</template>

<script>
import MoreOptions from "./QuickAccess/MoreOptions.vue"
import BatterySettings from "./QuickAccess/BatterySettings.vue"
import NetworkSettings from "./QuickAccess/NetworkSettings.vue"
import VolumeSettings from "./QuickAccess/VolumeSettings.vue"
import Notifications from "./QuickAccess/Notifications.vue"

export default {
    name: 'QuickAccess',
    props: ['time','date','day'],
    components: { MoreOptions, BatterySettings, NetworkSettings, VolumeSettings, Notifications,
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
      refresh(){
          window.location.reload();
      }
    },
}

</script>

<style scoped>

/* quick access container */
.quickAccess{
  --main-bg: #171617f0;
  --quick-access-hover: #ffffff26;
  --fg: #d6d6d6;
  --border: 2px solid #312e2e67;
  --bg: #201f20;

}
.access {
  position: absolute;
  right: 0;
  width: 15vw;
  height: 100%;
  display: flex;
  justify-content: space-evenly;
  align-items: center;
}
/* quick access icon container */
.access .accessContainer {
  display: flex;
  justify-content: center;
  align-items: center;
  width: 25px;
  height: 85%;
  border-radius: 5px;
  cursor: pointer;
  transition: 0.3s;
}
.accessContainer:hover,
.QACalendar:hover,
.home:hover {
  background: var(--quick-access-hover);
}
/* quick access icons */
.access .accessContainer i {
  color: var(--fg);
  transform: scale(0.9);
}
.access .accessContainer img {
  width: 1.1rem;
}
/* date,time container */
.access .QACalendar {
  display: flex;
  justify-content: center;
  flex-direction: column;
  width: 80px;
  height: 90%;
  border-radius: 5px;
  cursor: pointer;
  font-family: "Calibri", sans-serif;
  font-weight: 500;
  transition: 0.3s;

  z-index: 5;
}
/* QACalendar text part */
.access .QACalendar .QACalItem {
  text-align: center;
  color: var(--fg);
  font-size: 14px;
}

/* QACalendar date animation on hover */
.access .QACalendar:hover .date {
  opacity: 1;
  transform: translateY(0);
}
.access .QACalendar .date {
  position: absolute;
  top: -3rem;
  left: 6.5rem;
  padding: 0.5rem;
  border-radius: 5px;
  background: var(--main-bg);
  font-weight: 500;
  font-size: 0.9rem;
  color: var(--fg);

  opacity: 0;
  transform: translateY(50%);
  transition: opacity 0.5s 0.2s, transform 0.5s 0.2s;
  z-index: 3;
}
.access .QACalendar .date::after {
  content: "";
  position: absolute;
  bottom: -0.4rem;
  left: 50%;
  transform: translateX(-50%) rotate(45deg);
  width: 15px;
  height: 15px;
  border-radius: 2px;
  z-index: 0;
  background: var(--main-bg);
}

/* division at the end */
.access .home {
  cursor: pointer;
  transition: 0.5s;
  transform: translateX(5px);
  width: 10px;
  border-radius: 3px;
  height: 80%;
  border-left: none;
}
.access .home:hover {
  border-left: 2px solid rgba(255, 255, 255, 0.5);
}

</style>