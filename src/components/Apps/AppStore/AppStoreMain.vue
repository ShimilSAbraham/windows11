<template>
    <div class="appStoreMain">
        <div class="preview" :class="previewBackground">
            <div class="previewContainer">
                <div @click="previewBackground='greenGradient'" class="previewItems greenGradient"></div>
                <div @click="previewBackground='seeOffGradient'" class="previewItems seeOffGradient"></div>
                <div @click="previewBackground='clearSkyGradient'" class="previewItems clearSkyGradient"></div>
                <div @click="previewBackground='suzyGradient'" class="previewItems suzyGradient"></div>
                <div @click="previewBackground='purpleGradient'" class="previewItems purpleGradient"></div>
                <div @click="previewBackground='sweetMorningGradient'" class="previewItems sweetMorningGradient"></div>
            </div>
        </div>
        <TrendingApps />
    </div>
</template>

<script>
import TrendingApps from "./AppStoreMain/TrendingApps.vue";
export default {
    name:"AppStoreMain",
    components: {
        TrendingApps,
        },
        data(){
            return{
                previewBackground: 'greenGradient',
            }
        },
}
</script>

<style scoped>
.appStoreMain{
    position: absolute;
    top: 9%;
    left: 7%;
    width: 93%;
    height: 90%;
    border-radius: 10px;

    display: flex;
    align-items: center;
    flex-direction: column;
    justify-content: space-around;

    backdrop-filter: blur( 12px );
    -webkit-backdrop-filter: blur( 12px );

  }

.appStoreMain .preview{
    height: 60%;
    width: 98%;
    border-radius: 5px;

    display: flex;
    align-items: flex-end;
    justify-content: center;
}

.appStoreMain .previewContainer{
    width: 100%;
    height: 40%;

    display: flex;
    align-items: center;
    justify-content: space-evenly;
}
.appStoreMain .preview .previewItems{
    height: 85%;
    width: 16%;
    border-radius: 5px;
    transition: 0.5s;

}

.appStoreMain .preview .previewItems:hover{
    transform: scale(1.02);
    opacity: 0.6;
}

</style>