<template>
    <div>
        <h2>
            {{infoMessage}}
        </h2>
        <div>
            <svg width="284px" height="357px" viewBox="0 0 284 357" version="1.1" xmlns="http://www.w3.org/2000/svg" xmlns:xlink="http://www.w3.org/1999/xlink">
                <defs>
                    <circle id="path-1" cx="118.5" cy="158.5" r="17.5"></circle>
                    <filter x="-20.0%" y="-14.3%" width="140.0%" height="140.0%" filterUnits="objectBoundingBox" id="filter-2">
                        <feOffset dx="0" dy="2" in="SourceAlpha" result="shadowOffsetOuter1"></feOffset>
                        <feGaussianBlur stdDeviation="2" in="shadowOffsetOuter1" result="shadowBlurOuter1"></feGaussianBlur>
                        <feColorMatrix values="0 0 0 0 0   0 0 0 0 0   0 0 0 0 0  0 0 0 0.5 0" type="matrix" in="shadowBlurOuter1"></feColorMatrix>
                    </filter>
                    <circle id="path-3" cx="173.5" cy="158.5" r="17.5"></circle>
                    <filter x="-20.0%" y="-14.3%" width="140.0%" height="140.0%" filterUnits="objectBoundingBox" id="filter-4">
                        <feOffset dx="0" dy="2" in="SourceAlpha" result="shadowOffsetOuter1"></feOffset>
                        <feGaussianBlur stdDeviation="2" in="shadowOffsetOuter1" result="shadowBlurOuter1"></feGaussianBlur>
                        <feColorMatrix values="0 0 0 0 0   0 0 0 0 0   0 0 0 0 0  0 0 0 0.5 0" type="matrix" in="shadowBlurOuter1"></feColorMatrix>
                    </filter>
                </defs>
                <g id="Page-1" stroke="none" stroke-width="1" fill="none" fill-rule="evenodd">
                    <g id="Apple-TV" transform="translate(-636.000000, -469.000000)">
                        <g id="happy" transform="translate(636.000000, 463.000000)">
                            <g @click="toggleHappy" id="Group" opacity="0.801990327" fill="#F5A623">
                                <path d="M100,80 L184,80 C239.228475,80 284,124.771525 284,180 L284,355 C284,359.418278 280.418278,363 276,363 L8,363 C3.581722,363 5.41083001e-16,359.418278 0,355 L0,180 C-6.76353751e-15,124.771525 44.771525,80 100,80 Z" id="Rectangle"></path>
                                <rect id="Rectangle" transform="translate(211.000000, 70.000000) rotate(38.000000) translate(-211.000000, -70.000000) " x="191" y="19" width="40" height="102" rx="20"></rect>
                                <rect id="Rectangle" transform="translate(152.500000, 66.000000) rotate(27.000000) translate(-152.500000, -66.000000) " x="133" y="2" width="39" height="128" rx="19.5"></rect>
                                <rect id="Rectangle" transform="translate(94.500000, 70.000000) rotate(21.000000) translate(-94.500000, -70.000000) " x="75" y="6" width="39" height="128" rx="19.5"></rect>
                            </g>
                            // Auge Links
                            <g id="Oval">
                                <use fill="black" fill-opacity="1" filter="url(#filter-2)" xlink:href="#path-1"></use>
                                <use fill="#FFFFFF" fill-rule="evenodd" xlink:href="#path-1"></use>
                            </g>
                            // Auge Rechts
                            <g v-if="!this.eyepokedStatus" @click="pokeEye" id="Oval">
                                <use fill="black" fill-opacity="1" filter="url(#filter-4)" xlink:href="#path-3"></use>
                                <use fill="#FFFFFF" fill-rule="evenodd" xlink:href="#path-3"></use>
                            </g>
                            // Auge Rechts zu
                            <line v-if="this.eyepokedStatus" x1="157.5" y1="158.5" x2="187.5" y2="158.5" id="Line" stroke="#4A4A4A" stroke-width="5" stroke-linecap="round"></line>
                            // Pupillen
                            <circle :class="{ 'moving-eyes': happyStatus}" id="Oval" stroke="#979797" fill="#4A4A4A" cx="114" cy="158" r="4"></circle>
                            <circle v-if="!this.eyepokedStatus" :class="{ 'moving-eyes': happyStatus}" id="Oval" stroke="#979797" fill="#4A4A4A" cx="169" cy="158" r="4"></circle>
                            // Mund Traurig
                            <path v-if="!this.happyStatus && !this.whistleStatus" d="M59,215.333091 C65.0849402,239.631043 100.862006,259 144.08739,259 C187.851338,259 220.584191,239.145382 225.45858,214.422605" id="Path" stroke="#4A4A4A" stroke-width="5" stroke-linecap="round" transform="translate(142.229290, 236.711303) scale(1, -1) translate(-142.229290, -236.711303) "></path>
                            // Mund Happy
                            <path v-if="this.happyStatus && !this.whistleStatus" d="M56.91261,171.333091 C62.9975502,195.631043 98.7746163,215 142,215 C185.763948,215 218.496801,195.145382 223.37119,170.422605" id="Path" stroke="#4A4A4A" stroke-width="5" stroke-linecap="round"></path>

                            // Mund pfeiffen
                            <path  v-if="this.whistleStatus" d="M144,236 C144,230.477153 139.522847,226 134,226" id="whistle" stroke="#4A4A4A" transform="translate(139.000000, 231.000000) rotate(38.000000) translate(-139.000000, -231.000000) "></path>
                            <g :class="{ 'moving-mouth': whistleStatus}" v-if="this.whistleStatus" id="mouth">
                                <use fill="#4A4A4A" fill-rule="evenodd" xlink:href="#path-5"></use>
                                <use fill="black" fill-opacity="1" filter="url(#filter-6)" xlink:href="#path-5"></use>
                            </g>
                        </g>
                    </g>
                </g>
            </svg>

            <div hidden>
                <svg width="284px" height="357px" viewBox="0 0 284 357" version="1.1" xmlns="http://www.w3.org/2000/svg" xmlns:xlink="http://www.w3.org/1999/xlink">
                    <!-- Generator: Sketch 63.1 (92452) - https://sketch.com -->
                    <title>Page 1</title>
                    <desc>Created with Sketch.</desc>
                    <defs>
                        <circle id="path-1" cx="118.5" cy="158.5" r="17.5"></circle>
                        <filter x="-20.0%" y="-14.3%" width="140.0%" height="140.0%" filterUnits="objectBoundingBox" id="filter-2">
                            <feOffset dx="0" dy="2" in="SourceAlpha" result="shadowOffsetOuter1"></feOffset>
                            <feGaussianBlur stdDeviation="2" in="shadowOffsetOuter1" result="shadowBlurOuter1"></feGaussianBlur>
                            <feColorMatrix values="0 0 0 0 0   0 0 0 0 0   0 0 0 0 0  0 0 0 0.5 0" type="matrix" in="shadowBlurOuter1"></feColorMatrix>
                        </filter>
                        <circle id="path-3" cx="173.5" cy="158.5" r="17.5"></circle>
                        <filter x="-20.0%" y="-14.3%" width="140.0%" height="140.0%" filterUnits="objectBoundingBox" id="filter-4">
                            <feOffset dx="0" dy="2" in="SourceAlpha" result="shadowOffsetOuter1"></feOffset>
                            <feGaussianBlur stdDeviation="2" in="shadowOffsetOuter1" result="shadowBlurOuter1"></feGaussianBlur>
                            <feColorMatrix values="0 0 0 0 0   0 0 0 0 0   0 0 0 0 0  0 0 0 0.5 0" type="matrix" in="shadowBlurOuter1"></feColorMatrix>
                        </filter>
                        <circle id="path-5" cx="117.5" cy="234.5" r="12.5"></circle>
                        <filter x="-8.0%" y="-8.0%" width="116.0%" height="116.0%" filterUnits="objectBoundingBox" id="filter-6">
                            <feGaussianBlur stdDeviation="1.5" in="SourceAlpha" result="shadowBlurInner1"></feGaussianBlur>
                            <feOffset dx="0" dy="1" in="shadowBlurInner1" result="shadowOffsetInner1"></feOffset>
                            <feComposite in="shadowOffsetInner1" in2="SourceAlpha" operator="arithmetic" k2="-1" k3="1" result="shadowInnerInner1"></feComposite>
                            <feColorMatrix values="0 0 0 0 0   0 0 0 0 0   0 0 0 0 0  0 0 0 0.5 0" type="matrix" in="shadowInnerInner1"></feColorMatrix>
                        </filter>
                    </defs>
                    <g id="Page-1" stroke="none" stroke-width="1" fill="none" fill-rule="evenodd">
                        <g id="Apple-TV" transform="translate(-256.000000, -57.000000)">
                            <g id="mouth-open" transform="translate(256.000000, 51.000000)">
                                <g id="Group" opacity="0.798037574" fill="#F5A623">
                                    <path d="M100,80 L184,80 C239.228475,80 284,124.771525 284,180 L284,355 C284,359.418278 280.418278,363 276,363 L8,363 C3.581722,363 5.41083001e-16,359.418278 0,355 L0,180 C-6.76353751e-15,124.771525 44.771525,80 100,80 Z" id="Rectangle"></path>
                                    <rect id="Rectangle" transform="translate(211.000000, 70.000000) rotate(38.000000) translate(-211.000000, -70.000000) " x="191" y="19" width="40" height="102" rx="20"></rect>
                                    <rect id="Rectangle" transform="translate(152.500000, 66.000000) rotate(27.000000) translate(-152.500000, -66.000000) " x="133" y="2" width="39" height="128" rx="19.5"></rect>
                                    <rect id="Rectangle" transform="translate(94.500000, 70.000000) rotate(21.000000) translate(-94.500000, -70.000000) " x="75" y="6" width="39" height="128" rx="19.5"></rect>
                                </g>
                                <path d="M144,236 C144,230.477153 139.522847,226 134,226" id="whistle" stroke="#4A4A4A" transform="translate(139.000000, 231.000000) rotate(38.000000) translate(-139.000000, -231.000000) "></path>
                                <g id="eye-left">
                                    <use fill="black" fill-opacity="1" filter="url(#filter-2)" xlink:href="#path-1"></use>
                                    <use fill="#FFFFFF" fill-rule="evenodd" xlink:href="#path-1"></use>
                                </g>
                                <g id="eye-right">
                                    <use fill="black" fill-opacity="1" filter="url(#filter-4)" xlink:href="#path-3"></use>
                                    <use fill="#FFFFFF" fill-rule="evenodd" xlink:href="#path-3"></use>
                                </g>
                                <circle id="eye-left" stroke="#979797" fill="#4A4A4A" cx="114" cy="158" r="4"></circle>
                                <circle id="eye-right" stroke="#979797" fill="#4A4A4A" cx="169" cy="158" r="4"></circle>
                                <g id="mouth">
                                    <use fill="#4A4A4A" fill-rule="evenodd" xlink:href="#path-5"></use>
                                    <use fill="black" fill-opacity="1" filter="url(#filter-6)" xlink:href="#path-5"></use>
                                </g>
                            </g>
                        </g>
                    </g>
                </svg>
            </div>


        </div>
        <h1>
            Hi, <br>
            <span class="typer" id="first-typer" data-words="play some sound, poke me in my right eye" data-colors="#cd2032,#cc1e81,#6e6abb"></span>
            <span class="cursor" data-owner="first-typer"></span>
        </h1>
        <p @click="startMusic">playing music</p>
        <p @click="startWind">make some wind</p>
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
            eyepokedStatus: false,
            whistleStatus: false
        }),
        methods: {
            toggleHappy() {
                this.happyStatus = !this.happyStatus;
                this.infoMessage = (this.happyStatus ? 'happy' : 'not happy');
            },
            pokeEye() {
                this.infoMessage = 'Eye poke!';
                this.eyepokedStatus = true;
                this.happyStatus = false;
                setTimeout(() => {
                    this.eyepokedStatus = false;
                    this.infoMessage = (this.happyStatus ? 'happy' : 'not happy');
                    }, 2000);

            },
            startMusic() {
                this.infoMessage = 'music is playing';
                setTimeout(() => {
                    this.startWhistling();
                }, 2000);
            },
            stopMusic () {
                setTimeout(() => {
                    this.whistleStatus = false;
                    this.happyStatus = true;
                    this.infoMessage = (this.happyStatus ? 'happy' : 'not happy');
                }, 2000);
            },
            startWhistling() {
                this.infoMessage = 'whistling';
                this.whistleStatus = true;
                setTimeout(() => {
                    this.stopMusic();
                }, 4000);
            },
            startWind () {
                this.infoMessage = 'wind is blowing';
                setTimeout(() => {
                    this.happyStatus = false;
                    this.infoMessage = (this.happyStatus ? 'happy' : 'not happy');
                }, 4000);
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
    .moving-mouth{
        position: absolute;
        z-index: 2;
        height: 15%;
        width: 15%;
        top: 1%;
        left:5%;
        animation: mouthMove 1s infinite;
    }
    @keyframes mouthMove {
        0%   {    transform: rotateY(0deg)   }
        90%  {    width: 2em;        }
        100% {   transform: rotateY(-20deg)   }

    }

    @keyframes lookingAround {
        0%   {    transform: rotateX(10deg)   }
        10%  {    transform: rotateY(10deg)   }
        20%  {    transform: rotateY(10deg)   }
        30%  {    transform: rotateY(15deg)   }
        40%  {   transform: rotateX(10deg)    }
        50%  {   transform: rotateX(15deg)    }
        60%  {   transform: rotateX(-10deg)    }
        70%  {    transform: rotateX(-5deg)   }
        80%  {    transform: rotateX(0deg)   }
        90%  {   transform: rotateX(5deg)    }
        100% {   transform: rotateX(10deg)    }

    }

</style>
