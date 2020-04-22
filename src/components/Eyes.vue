<template>
    <div>
        <header class="header">
            <p class="musicButton" @click="startMusic">playing music</p>
            <p class="windButtonButton" @click="startWind">make some wind</p>
        </header>
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
                    <circle id="path-5" cx="117.5" cy="234.5" r="12.5"></circle>
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

                                <!-- Haare normal -->
                                <rect v-if="!this.windStatus" id="Rectangle" transform="translate(211.000000, 70.000000) rotate(38.000000) translate(-211.000000, -70.000000) " x="191" y="19" width="40" height="102" rx="20"></rect>
                                <rect v-if="!this.windStatus" id="Rectangle" transform="translate(152.500000, 66.000000) rotate(27.000000) translate(-152.500000, -66.000000) " x="133" y="2" width="39" height="128" rx="19.5"></rect>
                                <rect v-if="!this.windStatus" id="Rectangle" transform="translate(94.500000, 70.000000) rotate(21.000000) translate(-94.500000, -70.000000) " x="75" y="6" width="39" height="128" rx="19.5"></rect>

                                <!-- Haare Wind -->
                                <path v-if="this.windStatus" d="M237.411122,34.5906746 L238.423515,34.7428477 C242.993565,35.4297738 246.141459,39.6913953 245.454533,44.2614459 C245.274318,45.4603983 244.835713,46.6058687 244.169079,47.6185692 L238.147528,56.7660465 L238.147528,56.7660465 L228.561839,77.3456336 L226.328569,105.588574 C225.50606,115.990396 216.825095,124.012024 206.390804,124.012024 L204.871761,124.012024 C196.733309,124.012024 190.13579,117.414505 190.13579,109.276052 C190.13579,107.795738 190.358842,106.323873 190.797435,104.910024 L199.355686,77.321654 L199.355686,77.321654 L210.091995,53.705311 L218.331687,42.5119953 C222.729967,36.5370946 230.074355,33.4878822 237.411122,34.5906746 Z" id="hair3" transform="translate(218.118078, 78.404861) rotate(38.000000) translate(-218.118078, -78.404861) "></path>
                                <path v-if="this.windStatus" d="M189.232611,11.7342122 L189.419084,11.7603928 C194.289717,12.4442238 197.68379,16.9470061 196.999959,21.8176385 C196.871673,22.7313616 196.602169,23.6195982 196.201093,24.4505525 L187.857739,41.7364199 L187.857739,41.7364199 L169.103869,73.6302559 L169.103869,113.584024 C169.103869,124.353576 160.373422,133.084024 149.603869,133.084024 C140.114333,133.084024 132.421543,125.391234 132.421543,115.901698 C132.421543,115.178673 132.46718,114.456368 132.558182,113.739093 L135.458099,90.8818949 L135.458099,90.8818949 L143.307413,64.4359449 L160.520783,34.3410965 L170.48947,19.9440781 C174.684199,13.8859495 181.935552,10.7097138 189.232611,11.7342122 Z" id="hair2" transform="translate(165.805476, 71.573638) rotate(27.000000) translate(-165.805476, -71.573638) "></path>
                                <path v-if="this.windStatus" d="M129.156899,18.3756812 L130.360265,18.5803102 C135.73454,19.49419 139.350404,24.5917461 138.436524,29.9660206 C138.18847,31.4247577 137.61563,32.8090627 136.760378,34.0165348 L127.074496,47.6913686 L127.074496,47.6913686 C123.023043,58.6157284 119.38003,66.7980681 116.145459,72.2383877 C112.910888,77.6787073 111.333931,78.2759873 111.414588,74.0302275 L111.414588,116.399443 C111.414588,127.168995 102.684141,135.899443 91.9145881,135.899443 C82.988726,135.899443 75.7528851,128.663602 75.7528851,119.73774 C75.7528851,118.73134 75.8468884,117.72714 76.0336701,116.738226 L82.178196,84.2060535 L82.178196,84.2060535 L100.368151,45.0892343 L108.435101,28.9020454 C112.268226,21.2104735 120.684732,16.9350139 129.156899,18.3756812 Z" id="hair1" transform="translate(109.122566, 75.924538) rotate(21.000000) translate(-109.122566, -75.924538) "></path>
                            </g>

                            <!-- Auge Links -->
                            <g id="Oval">
                                <use fill="black" fill-opacity="1" filter="url(#filter-2)" xlink:href="#path-1"></use>
                                <use fill="#FFFFFF" fill-rule="evenodd" xlink:href="#path-1"></use>
                            </g>

                            <!-- Auge Rechts -->
                            <g v-if="!this.eyepokedStatus" @click="pokeEye" id="Oval">
                                <use fill="black" fill-opacity="1" filter="url(#filter-4)" xlink:href="#path-3"></use>
                                <use fill="#FFFFFF" fill-rule="evenodd" xlink:href="#path-3"></use>
                            </g>

                            <!-- Auge Rechts zu -->
                            <line v-if="this.eyepokedStatus" x1="157.5" y1="158.5" x2="187.5" y2="158.5" id="Line" stroke="#4A4A4A" stroke-width="5" stroke-linecap="round"></line>

                            <!-- Pupillen -->
                            <circle :class="{ 'moving-eyes': happyStatus}" id="Oval" stroke="#979797" fill="#4A4A4A" cx="114" cy="158" r="4"></circle>
                            <circle v-if="!this.eyepokedStatus" :class="{ 'moving-eyes': happyStatus}" id="Oval" stroke="#979797" fill="#4A4A4A" cx="169" cy="158" r="4"></circle>

                            <!-- Mund Traurig -->
                            <path v-if="!this.happyStatus && !this.whistleStatus && !this.windStatus" d="M59,215.333091 C65.0849402,239.631043 100.862006,259 144.08739,259 C187.851338,259 220.584191,239.145382 225.45858,214.422605" id="Path" stroke="#4A4A4A" stroke-width="5" stroke-linecap="round" transform="translate(142.229290, 236.711303) scale(1, -1) translate(-142.229290, -236.711303) "></path>

                            <!-- Mund Happy -->
                            <path v-if="this.happyStatus && !this.whistleStatus && !this.windStatus" d="M56.91261,171.333091 C62.9975502,195.631043 98.7746163,215 142,215 C185.763948,215 218.496801,195.145382 223.37119,170.422605" id="Path" stroke="#4A4A4A" stroke-width="5" stroke-linecap="round"></path>

                            <!-- Mund pfeiffen -->
                            <path  v-if="this.whistleStatus" d="M144,236 C144,230.477153 139.522847,226 134,226" id="whistle" stroke="#4A4A4A" transform="translate(139.000000, 231.000000) rotate(38.000000) translate(-139.000000, -231.000000) "></path>
                            <g :class="{ 'moving-mouth': whistleStatus}" v-if="this.whistleStatus" id="mouth">
                                <use fill="#4A4A4A" fill-rule="evenodd" xlink:href="#path-5"></use>
                                <use fill="black" fill-opacity="1" filter="url(#filter-6)" xlink:href="#path-3"></use>
                            </g>
                            <!-- Mund wind -->
                            <g v-if="this.windStatus" id="mund">
                                <use fill="#4A4A4A" fill-rule="evenodd" xlink:href="#path-5"></use>
                                <use fill="black" fill-opacity="1" filter="url(#filter-6)" xlink:href="#path-5"></use>
                            </g>
                        </g>
                    </g>
                </g>
            </svg>
        </div>
    </div>
</template>

<script>
    export default {
        data:() => ({
            color: '#EDD60C',
            happyStatus: false,
            infoMessage: 'not happy',
            eyepokedStatus: false,
            whistleStatus: false,
            windStatus: false
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
                this.windStatus = true;
                // TODO: Ein Haar sollte ausfallen und dann langsam wieder wachsen
                setTimeout(() => {
                    this.windStatus = false;
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
    .musicButton {
        float: left;
        margin-left: 20px;
    }
    .windButtonButton {
        float: right;
        margin-right: 20px;
    }

</style>
