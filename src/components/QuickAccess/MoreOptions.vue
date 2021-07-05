<template>
    <div class="moreOptions">
        <div class="hiddenIcon">
            <img src="../../assets/svg/html5.svg" alt="html5" />
        </div>
        <div class="hiddenIcon">
            <img src="../../assets/svg/css3.svg" alt="css3" />
        </div>
        <div class="hiddenIcon">
            <img src="../../assets/svg/javascript.svg" alt="javascript" />
        </div>
       <div class="hiddenIcon">
           <img src="../../assets/svg/vue.svg" alt="vue" />
        </div>
        <div class="hiddenIcon">
           <img src="../../assets/svg/github.svg" alt="vue" />
       </div>
       <div class="hiddenIcon"></div>
    </div>
</template>

<script>
export default {
    name: 'MoreOptions',
}
</script>

<style>
    .moreOptions {
        position: absolute;
        top: -235%;
        left: -27%;

        width: 150px;
        height: 100px;
        padding: 3px;  
        border-radius: 8px;

        background-color: var(--main-bg);
        border: var(--border);

        display: flex;
        justify-content: space-evenly;
        align-content: space-around;
        flex-wrap: wrap; 
    }

    .hiddenIcon {
        width: 2.5rem;
        height: 2.5rem;
        background-color: var(--bg);
        border-radius: 5px;
        display: flex;
        align-items: center;
        justify-content: center; 

        cursor: pointer;
        transition: background-color 0.3s ease;
    }

    .hiddenIcon:hover{
        background-color: var(--quick-access-hover);
    }

    .hiddenIcon > img {
        width:1.7rem;
        height: 1.7rem;
}
</style>