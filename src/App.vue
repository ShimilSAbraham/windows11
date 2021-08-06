<template>
  <Mobile :time="time" :date="date" :day="day" />

  <video autoplay muted id="vid">
        <source src="./assets/intro.webm" type="video/webm">
  </video>

  <Taskbar :time="time" :date="date" :day="day" />
</template>

<script>
import Mobile from "./components/Mobile.vue"
import Taskbar from "./components/Taskbar.vue"

export default {
  name: 'App',
  components: {
    Mobile,
    Taskbar,
  },
  data(){
      return{
          date : "",
          time : "",
          day : "",
      }
  },
  mounted() {
      this.updateClock();
      window.setInterval(this.updateClock,1000)
  },
  methods: {
      updateClock() {
      let d = new Date();

      let date = `${(this.addZero(d.getDate()))} ${(this.monthName(d.getMonth()))} ${(d.getFullYear())}`;
      let time = `${(this.addZero(d.getHours()))}:${(this.addZero(d.getMinutes()))}`;

      this.day = this.dayName(d.getDay());
      this.date = date;
      this.time = time;
      },

      addZero(num) {
      if (num < 10) return "0" + num;
      else return num;
      },

      dayName(num) {
      let week = ["Sunday","Monday","Tuesday","Wednesday","Thursday","Friday","Saturday",];
      return week[num];
      },
      
      monthName(num) {
      let months = ["Jan","Feb","March","April","May","June","July","Aug","Sept","Oct","Nov","Dec",];
      return months[num];
      },
  },
}

</script>

<style>

#app {
  --color: #198f85;
  --color-70: #198f8570;

  font-family: 'Open Sans','Nunito', sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;

  width: 100vw;
  height: 100vh;

  display: flex;
  align-items: flex-end;
  overflow: hidden;
}

#app #vid{
	position: absolute;
	width: 80%;
	left: 50%;
	top: 55%;
	transform: translate(-50%,-50%);	
}

</style>
