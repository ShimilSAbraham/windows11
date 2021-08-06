<template>
    <div class="appStoreMain">
        <div class="preview" :class="previewBackground">
            <div class="previewContainer">
                <div @click="smooth('lucaPreview')" class="previewItems lucaPreview"></div>
                <div @click="smooth('microsoft365Preview')" class="previewItems microsoft365Preview"></div>
                <div @click="smooth('spotifyPreview')" class="previewItems spotifyPreview"></div>
                <div @click="smooth('amazonPreview')" class="previewItems amazonPreview"></div>
                <div @click="smooth('lottiePreview')" class="previewItems lottiePreview"></div>
                <div @click="smooth('netflixPreview')" class="previewItems netflixPreview"></div>
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
                previewBackground: 'lucaPreview',
            }
        },
        methods: {
            smooth(image) {
                this.previewBackground = image;
            },
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

    transition: background-image 0.1s ease-in-out;
}

.appStoreMain .previewContainer{
    width: 100%;
    height: 35%;

    display: flex;
    align-items: center;
    justify-content: space-evenly;
}
.appStoreMain .preview .previewItems{
    height: 85%;
    width: 16%;
    border-radius: 5px;
    cursor: pointer;
    opacity: 0.8;
    transition: 0.5s;

}

.appStoreMain .preview .previewItems:hover{
    transform: scale(1.02);
    opacity: 0.6;
}

</style>