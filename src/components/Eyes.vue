<template>
    <div>
        <p>click me!</p>
        <div>
            <svg width=50% height=50% viewBox="0 0 200 200" fill="none" xmlns="http://www.w3.org/2000/svg">
                // Hintergrund
                <circle @click="toggleHappy" cx="100" cy="100" r="100" :fill="color"/>
                // Linkes Auge
                <circle cx="62" cy="50" r="15" fill="white"/>
                // Rechtes Auge auf
                <circle v-if="!this.eyepokedStatus" @click="pokeEye" cx="135" cy="50" r="15" fill="white"/>
                // Rechtes Auge zu
                <ellipse v-if="this.eyepokedStatus" cx="130.5" cy="48" rx="15" ry="1" fill="white"/>
                // Mund gerade
                <line v-if="!this.happyStatus" x1="30" y1="123.5" x2="170" y2="123.5" stroke="white" stroke-width="7"/>
                // Mund Happy
                <path v-if="this.happyStatus" d="M30 121.5L46.3813 141.189C52.655 148.73 61.0079 154.258 70.4003 157.086L85.5827 161.658C94.9857 164.49 105.014 164.49 114.417 161.658L129.6 157.086C138.992 154.258 147.345 148.73 153.619 141.189L170 121.5" stroke="white" stroke-width="7"/>
                // Pupille Rechts
                <circle v-if="!this.eyepokedStatus" :class="{ 'moving-eyes': happyStatus}" cx="137.5" cy="57.5" r="4.5" fill="black"/>
                // Pupille Links
                <circle :class="{ 'moving-eyes': happyStatus}" cx="66.5" cy="57.5" r="4.5" fill="black"/>
            </svg>


        </div>
        <p></p>
        <h1>
            {{infoMessage}}
        </h1>
        <h1>
            Hi,
            <span class="typer" id="first-typer" data-words="please click me,poke me in my right eye" data-colors="#cd2032,#cc1e81,#6e6abb"></span>
            <span class="cursor" data-owner="first-typer"></span>
        </h1>
    </div>
</template>

<script>
    export default {
        name: 'HelloWorld',
        created() {
            let typer = document.createElement('script');    typer.setAttribute('src',"https://unpkg.com/typer-dot-js@0.1.0/typer.js");
            document.head.appendChild(typer);
        },
        data:() => ({
            color: '#EDD60C',
            happyStatus: false,
            infoMessage: 'not happy',
            eyepokedStatus: false
        }),
        methods: {
            toggleHappy() {
                this.happyStatus = !this.happyStatus;
                this.infoMessage = (this.happyStatus ? 'is happy' : 'not happy');
            },
            pokeEye() {
                this.infoMessage = 'Eye poke!';
                this.eyepokedStatus = true;
                this.happyStatus = false;
                setTimeout(() => {
                    this.eyepokedStatus = false;
                    this.infoMessage = (this.happyStatus ? 'is happy' : 'not happy');
                    }, 2000);

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
