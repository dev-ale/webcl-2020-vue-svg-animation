<template>
    <div>
        <p>click me!</p>
        <div>
            <svg width=50% height=50% viewBox="0 0 200 200" fill="none" xmlns="http://www.w3.org/2000/svg">
                <circle @click="toggleHappy" cx="100" cy="100" r="100" :fill="color"/>
                <circle cx="62" cy="50" r="15" fill="white"/>
                <circle cx="135" cy="50" r="15" fill="white"/>
                <line v-if="!this.happyStatus" x1="30" y1="123.5" x2="170" y2="123.5" stroke="white" stroke-width="7"/>
                <path v-if="this.happyStatus" d="M30 121.5L46.3813 141.189C52.655 148.73 61.0079 154.258 70.4003 157.086L85.5827 161.658C94.9857 164.49 105.014 164.49 114.417 161.658L129.6 157.086C138.992 154.258 147.345 148.73 153.619 141.189L170 121.5" stroke="white" stroke-width="7"/>
                <circle :class="{ 'moving-eyes': happyStatus}" cx="137.5" cy="57.5" r="4.5" fill="black"/>
                <circle :class="{ 'moving-eyes': happyStatus}" cx="66.5" cy="57.5" r="4.5" fill="black"/>
            </svg>


        </div>
        <p>{{happyMessage}}</p>
    </div>
</template>

<script>
    export default {
        name: 'HelloWorld',
            data:() => ({
                color: '#EDD60C',
                happyStatus: false,
                happyMessage: 'not happy'
            }),
            methods: {
                toggleHappy() {
                    this.happyStatus = !this.happyStatus;
                    this.happyMessage = (this.happyStatus ? 'is happy' : 'not happy');
                }
            }
    }

</script>

<style>
    .moving-eyes{
        position: absolute;
        z-index: 2;
        height: 15%;
        width: 15%;
        top: 1%;
        left:5%;
        animation: lookingAround 4s infinite;
    }

    @keyframes lookingAround {
        0%   {    transform: rotateX(20deg)   }
        10%  {    transform: rotateY(15deg)   }
        20%  {    transform: rotateY(20deg)   }
        30%  {    transform: rotateY(15deg)   }
        40%  {   transform: rotateX(20deg)    }
        50%  {   transform: rotateX(25deg)    }
        60%  {   transform: rotateX(30deg)    }
        70%  {    transform: rotateX(35deg)   }
        80%  {    transform: rotateX(40deg)   }
        90%  {   transform: rotateX(30deg)    }
        100% {   transform: rotateX(25deg)    }

    }

</style>
