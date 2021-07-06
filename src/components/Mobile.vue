<template>
    <div class="mobile">
        <div class="mobCalendar">
            <div class="mobTime">{{time}}</div>
            <div class="mobDay">{{day}}</div>
            <div class="mobDate"> {{date}} </div>
        </div>

        <div class="cube">
            <div class="front blue-l"></div>
            <div class="side blue-d "></div>
            <div class="top blue"></div>
        </div>


        <div class="mobMessage">Sorry, couldn't load windows 11 on this device ...</div>	
    </div>
</template>

<script>
export default {
    name: 'Mobile',
    props: ['time','date','day'],
    
}
</script>

<style>

    .mobile{
        display: none;
    }

    @media (max-width:1000px){
        #app{
            font-family: 'Nunito', sans-serif !important;
            background: url('../assets/windows_11_bg_dark.jpg');
            background-position: center;
            background-repeat: no-repeat;

            color: #dfdddd;
            align-items: flex-start !important;
            justify-content: center !important;
            /* height: 25vh !important; */
        }
        #app #vid{
            display: none !important;
        }
        .taskbar{
            display: none !important;
        }
        .mobile{
            display: flex;
            flex-direction: column;
            align-items: center;
            justify-content: space-evenly;

            margin-top: 7px;
            font-size: 1.1rem;
            height: 80%;
        }
        .mobile .mobCalendar{
            display: flex;
            flex-direction: column;
            align-items: center;
            justify-content: center;
            height: 30%;
        }
        .mobile .mobTime{
            font-size: 4.5rem;
            font-weight: 600;
        }
        .mobile .mobDay{
            margin-top: -15px;
        }
        .mobile .mobDate{
            margin-bottom: 30px;
            margin-top: 10px;
        }
        .mobile .cube{
            align-self: center;
        }

        .mobile .mobMessage{

            font-size: 1.7rem;
            font-weight: 800;
            width: 70%;
            line-height: 2.3rem;

            text-shadow: -3px -3px 2px rgba(0, 0, 0, 0.493);
            color: #cacdd6;
            letter-spacing: 1.5px;
        }
    }
</style>
