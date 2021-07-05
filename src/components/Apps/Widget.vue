<template>
  <div class="widget">
      <h1>{{time}}</h1>
      <h3>{{day}}</h3>

      <div class="search">
      <i class="fad fa-search"></i>
      <input type="text" placeholder="Search for widgets..." />
    </div>
  </div>
</template>

<script>
export default {
    name: 'Widget',
    props: ['time','day'],
}
</script>

<style scoped>
    .widget{
        --inputs: #b6b6b6;

        --search-shadow: 0px 0px 4px 1px #00000099;
        --icons-active: #e4e4e4;

        position: absolute;
        top: -93vh;
        left: 0.5%;
        width: 32vw;
        border-radius: 10px;
        height: 92vh;
        background: #171617f0;

        display: flex;
        justify-content: center;
        align-items: center;

        border: var(--border);
        z-index: -5;
        backdrop-filter: blur( 12px );
        -webkit-backdrop-filter: blur( 12px );

    }
    .widget h1,h3{
        position: absolute;
        top: 5%;
        left: 50%;
        font-size: 3rem;
        transform: translateX(-50%);
        color: var(--inputs);
    }
    .widget h3{
        top: 15%;
        font-size: 1.5rem;
    }
    .widget .search {
    background: var(--bg);
    box-shadow: var(--search-shadow);
    width: 90%;
    border-radius: 5px;
    padding: 5px;
    height: 2.2rem;

    transform: translateY(-150px);

    display: flex;
    justify-content: space-around;
    align-items: center;
    }
    .widget .search i {
    transform: rotate(90deg);
    color: var(--icons-active);
    }
    .widget .search input {
    width: 90%;
    background: transparent;
    outline: none;
    border: none;
    font-size: 15px;
    color: var(--icons-active);
    }
    .widget .search input[type="text"]:focus {
    font-size: 15px;
    background-color: transparent;
    caret-color: var(--inputs);
    }
    .widget .search::placeholder {
    font-size: 15px;
    color: var(--inputs);
    opacity: 0.5;
    }
</style>