<template>
    <div>
        <header>
            <div class="musicButton" @click="startMusic">
                <svg :class="{ 'animate-radio': musicStatus}" width="50px" height="50px" version="1.1" id="Capa_1" xmlns="http://www.w3.org/2000/svg" xmlns:xlink="http://www.w3.org/1999/xlink" x="0px" y="0px"
                     viewBox="0 0 511.999 511.999" style="enable-background:new 0 0 511.999 511.999;" xml:space="preserve">
                <path style="fill:#394049;" d="M413.861,172.522h-32.079v-45.456c0-3.997-3.253-7.25-7.25-7.25H137.474
                    c-3.997,0-7.25,3.253-7.25,7.25v45.456H98.145v-45.456c0-21.686,17.644-39.329,39.329-39.329h237.058
                    c21.686,0,39.329,17.644,39.329,39.329V172.522z"/>
                    <path style="fill:#76C9D2;" d="M480.77,172.522H31.229c-12.819,0-23.211,10.392-23.211,23.211v205.32
                    c0,12.819,10.392,23.211,23.211,23.211h449.54c12.819,0,23.211-10.392,23.211-23.211V195.731
                    C503.98,182.913,493.589,172.522,480.77,172.522z"/>
                    <path style="opacity:0.15;enable-background:new    ;" d="M8.02,392.592v8.459c0,12.819,10.392,23.211,23.211,23.211h449.54
                    c12.819,0,23.211-10.392,23.211-23.211v-8.459H8.02z"/>
                    <circle style="fill:#0081C6;" cx="109.69" cy="290.907" r="80.733"/>
                    <circle style="fill:#394049;" cx="109.69" cy="290.907" r="59.176"/>
                    <circle style="fill:#0081C6;" cx="402.309" cy="290.907" r="80.733"/>
                    <circle style="fill:#394049;" cx="402.309" cy="290.907" r="59.176"/>
                    <g>
                    <path style="fill:#E6595A;" d="M204.978,234.235h-17.042c-4.43,0-8.02-3.59-8.02-8.02s3.59-8.02,8.02-8.02h17.042
                        c4.43,0,8.02,3.59,8.02,8.02C212.998,230.644,209.408,234.235,204.978,234.235z"/>
                        <path style="fill:#E6595A;" d="M324.07,234.235h-17.043c-4.43,0-8.02-3.59-8.02-8.02s3.59-8.02,8.02-8.02h17.043
                        c4.43,0,8.02,3.59,8.02,8.02C332.09,230.644,328.499,234.235,324.07,234.235z"/>
                </g>
                    <path style="opacity:0.15;enable-background:new    ;" d="M286.058,298.388h-60.11c-4.394,0-7.955,3.562-7.955,7.955v19.863
                    c0,4.394,3.562,7.955,7.955,7.955h60.11c4.393,0,7.955-3.562,7.955-7.955v-19.863C294.013,301.948,290.452,298.388,286.058,298.388z
                    "/>
                    <path style="fill:#394049;" d="M231.85,392.592h-20.105c-2.235,0-4.047-1.813-4.047-4.047v-16.058c0-2.235,1.813-4.047,4.047-4.047
                    h20.105V392.592z"/>
                    <rect x="231.849" y="368.443" style="fill:#E6595A;" width="24.153" height="24.153"/>
                    <rect x="256.005" y="368.443" style="fill:#394049;" width="24.153" height="24.153"/>
                    <path style="fill:#FFFFFF;" d="M300.262,392.592h-20.105V368.44h20.105c2.236,0,4.047,1.813,4.047,4.047v16.058
                    C304.309,390.78,302.496,392.592,300.262,392.592z"/>
                    <rect x="176.608" y="87.737" style="fill:#76C9D2;" width="158.783" height="32.079"/>
                    <path d="M246.005,228.528c3.696,0,7.137-1.119,9.999-3.036c2.863,1.917,6.304,3.036,9.999,3.036c9.936,0,18.02-8.084,18.02-18.019
                    c0-4.43-3.59-8.02-8.02-8.02s-8.02,3.59-8.02,8.02c0,1.091-0.889,1.979-1.98,1.979c-1.092,0-1.979-0.888-1.979-1.979
                    c0-4.43-3.59-8.02-8.02-8.02c-4.43,0-8.02,3.59-8.02,8.02c0,1.091-0.888,1.979-1.979,1.979s-1.98-0.888-1.98-1.979
                    c0-4.43-3.59-8.02-8.02-8.02c-4.43,0-8.02,3.59-8.02,8.02C227.984,220.444,236.068,228.528,246.005,228.528z M402.311,202.156
                    c-48.938,0-88.751,39.813-88.751,88.751s39.813,88.751,88.751,88.751s88.751-39.813,88.751-88.751
                    C491.062,241.968,451.249,202.156,402.311,202.156z M402.311,363.618c-40.093,0-72.711-32.618-72.711-72.711
                    s32.618-72.711,72.711-72.711s72.711,32.618,72.711,72.711C475.022,331,442.405,363.618,402.311,363.618z M286.058,290.368h-60.109
                    c-8.808,0-15.974,7.167-15.974,15.976v19.861c0,8.808,7.167,15.976,15.974,15.976h60.109c8.808,0,15.975-7.167,15.975-15.976
                    v-19.861C302.032,297.534,294.866,290.368,286.058,290.368z M226.013,326.205l-0.065-19.797h60.044l0.065,19.732L226.013,326.205z
                     M294.013,260.787h-76.026c-4.43,0-8.02,3.59-8.02,8.02s3.59,8.02,8.02,8.02h76.026c4.43,0,8.02-3.59,8.02-8.02
                    C302.032,264.377,298.443,260.787,294.013,260.787z M480.77,164.502h-58.888v-37.436c0-26.108-21.241-47.349-47.349-47.349H137.474
                    c-26.108,0-47.349,21.241-47.349,47.349v37.436H31.229C14.01,164.502,0,178.512,0,195.731v205.32c0,17.221,14.01,31.23,31.229,31.23
                    h449.54c17.22,0,31.229-14.01,31.229-31.23v-205.32C512,178.512,497.99,164.502,480.77,164.502z M343.412,95.757h31.12
                    c17.265,0,31.31,14.045,31.31,31.31v37.436h-16.04v-37.436c0-8.42-6.85-15.27-15.27-15.27h-31.12V95.757z M373.762,127.836v36.666
                    H138.243v-36.666H373.762z M184.633,95.757h142.739v16.04H184.633V95.757z M106.164,127.066c0-17.265,14.045-31.31,31.31-31.31
                    h31.12v16.04h-31.12c-8.42,0-15.27,6.85-15.27,15.27v37.436h-16.04V127.066z M495.96,401.052c0,8.376-6.814,15.191-15.19,15.191
                    H31.23c-8.376,0-15.19-6.815-15.19-15.191v-205.32c0-8.376,6.814-15.19,15.19-15.19h449.54c8.376,0,15.19,6.814,15.19,15.19V401.052
                    z M109.695,202.156c-48.938,0-88.751,39.813-88.751,88.751s39.813,88.751,88.751,88.751s88.751-39.813,88.751-88.751
                    S158.633,202.156,109.695,202.156z M109.695,363.618c-40.093,0-72.711-32.618-72.711-72.711s32.618-72.711,72.711-72.711
                    s72.711,32.618,72.711,72.711S149.788,363.618,109.695,363.618z M402.311,223.713c-37.051,0-67.194,30.143-67.194,67.194
                    s30.142,67.194,67.194,67.194c37.05,0,67.193-30.143,67.193-67.194S439.361,223.713,402.311,223.713z M402.311,342.061
                    c-28.206,0-51.154-22.948-51.154-51.154s22.948-51.154,51.154-51.154c28.205,0,51.153,22.948,51.153,51.154
                    C453.464,319.113,430.516,342.061,402.311,342.061z M196.458,195.339c-4.43,0-8.02,3.59-8.02,8.02v2.794c0,4.43,3.59,8.02,8.02,8.02
                    c4.43,0,8.02-3.59,8.02-8.02v-2.794C204.478,198.928,200.887,195.339,196.458,195.339z M323.568,206.153v-2.794
                    c0-4.43-3.59-8.02-8.02-8.02s-8.02,3.59-8.02,8.02v2.794c0,4.43,3.59,8.02,8.02,8.02
                    C319.978,214.173,323.568,210.583,323.568,206.153z M109.695,223.713c-37.051,0-67.194,30.143-67.194,67.194
                    S72.643,358.1,109.695,358.1s67.194-30.143,67.194-67.194S146.745,223.713,109.695,223.713z M109.695,342.061
                    c-28.206,0-51.154-22.948-51.154-51.154s22.948-51.154,51.154-51.154s51.154,22.948,51.154,51.154
                    C160.849,319.113,137.901,342.061,109.695,342.061z"/>
                </svg>
            </div>
            <div class="windButtonButton" @click="startWind">
                <div class="svgCombined">
                    <!-- Fan Hintergrund SVG-->
                    <svg style="position: absolute" width="50px" height="50px" viewBox="0 0 512 512" version="1.1" xmlns="http://www.w3.org/2000/svg" xmlns:xlink="http://www.w3.org/1999/xlink">
                        <g id="Page-1" stroke="none" stroke-width="1" fill="none" fill-rule="evenodd">
                            <g id="Artboard" transform="translate(-884.000000, -788.000000)" fill-rule="nonzero">
                                <g id="fan" transform="translate(884.000000, 788.000000)">
                                    <path d="M502,50 L502,462 C502,484.089844 484.089844,502 462,502 L50,502 C27.910156,502 10,484.089844 10,462 L10,50 C10,27.910156 27.910156,10 50,10 L462,10 C484.089844,10 502,27.910156 502,50 Z" id="Path" fill="#E0F4FF"></path>
                                    <path d="M256,56 C143.496094,56 58.292969,146.300781 56.050781,251.609375 C53.765625,362.039062 141.324219,456 256,456 C363.3125,456 456,370.273438 456,256 C456,145.539062 366.460938,56 256,56 Z" id="Path" fill="#7C8388"></path>
                                    <path d="M295.921875,253.5 C295.96875,254.328125 296,255.160156 296,256 C296,277.25 279.421875,294.628906 258.5,295.921875 C257.671875,295.96875 256.839844,296 256,296 C234.75,296 217.371094,279.421875 216.078125,258.5 C216.03125,257.671875 216,256.839844 216,256 C216,234.75 232.578125,217.371094 253.5,216.078125 C254.328125,216.03125 255.160156,216 256,216 C277.25,216 294.628906,232.578125 295.921875,253.5 Z" id="Path" fill="#E0F4FF"></path>
                                    <path d="M462,40 C456.480469,40 452,44.480469 452,50 C452,55.519531 456.480469,60 462,60 C467.519531,60 472,55.519531 472,50 C472,44.480469 467.519531,40 462,40 Z" id="Path" fill="#000000"></path>
                                    <path d="M462,452 C456.480469,452 452,456.480469 452,462 C452,467.519531 456.480469,472 462,472 C467.519531,472 472,467.519531 472,462 C472,456.480469 467.519531,452 462,452 Z" id="Path" fill="#000000"></path>
                                    <path d="M50,60 C55.519531,60 60,55.519531 60,50 C60,44.480469 55.519531,40 50,40 C44.480469,40 40,44.480469 40,50 C40,55.519531 44.480469,60 50,60 Z" id="Path" fill="#000000"></path>
                                    <path d="M50,452 C44.480469,452 40,456.480469 40,462 C40,467.519531 44.480469,472 50,472 C55.519531,472 60,467.519531 60,462 C60,456.480469 55.519531,452 50,452 Z" id="Path" fill="#000000"></path>
                                    <path d="M56,266 L56.25,266 C61.660156,265.859375 66,261.441406 66,256 C66,250.558594 61.660156,246.140625 56.25,246 C56.171875,246 56.078125,246 56,246 C50.480469,246 46,250.480469 46,256 C46,261.519531 50.480469,266 56,266 Z" id="Path" fill="#000000"></path>
                                    <path d="M462,0 L50,0 C22.429688,0 0,22.429688 0,50 L0,462 C0,489.570312 22.429688,512 50,512 L462,512 C489.570312,512 512,489.570312 512,462 L512,50 C512,22.429688 489.570312,0 462,0 Z M492,462 C492,478.542969 478.542969,492 462,492 L50,492 C33.457031,492 20,478.542969 20,462 L20,50 C20,33.457031 33.457031,20 50,20 L462,20 C478.542969,20 492,33.457031 492,50 L492,462 Z" id="Shape" fill="#000000"></path>
                                    <path d="M256,46 C153.976562,46 69.792969,118.140625 50.160156,214.1875 C49.058594,219.597656 52.546875,224.882812 57.957031,225.988281 C63.367188,227.089844 68.652344,223.601562 69.757812,218.191406 C87.78125,130.007812 166.105469,66 256,66 C360.765625,66 446,151.234375 446,256 C446,360.765625 360.765625,446 256,446 C165.546875,446 88.949219,383.378906 69.738281,293.714844 C68.582031,288.316406 63.261719,284.875 57.863281,286.03125 C52.464844,287.1875 49.023438,292.503906 50.179688,297.90625 C70.746094,393.875 152.417969,466 256,466 C372.34375,466 466,372.429688 466,256 C466,140.207031 371.792969,46 256,46 Z" id="Path" fill="#000000"></path>
                                </g>
                            </g>
                        </g>
                    </svg>
                    <!-- Fan Propeller SVG-->
                    <svg style="position: absolute" :class="{ 'animate-fan': windStatus}" height="50px" viewBox="0 0 512 512" width="50px" xmlns="http://www.w3.org/2000/svg">
                        <!--Ventilator (rotate this)-->
                        <!--TODO: rotation funktioniert noch nicht richtig (1/2)-->
                        <path  d="m296 256c0-.839844-.03125-1.671875-.078125-2.5 34.546875-8.851562 60.078125-40.199219 60.078125-77.5 0-44.179688-35.820312-80-80-80h-20v120c-.839844 0-1.671875.03125-2.5.078125-8.851562-34.546875-40.199219-60.078125-77.5-60.078125-44.179688 0-80 35.820312-80 80v20h120c0 .839844.03125 1.671875.078125 2.5-34.546875 8.851562-60.078125 40.199219-60.078125 77.5 0 44.179688 35.820312 80 80 80h20v-120c.839844 0 1.671875-.03125 2.5-.078125 8.851562 34.546875 40.199219 60.078125 77.5 60.078125 44.179688 0 80-35.820312 80-80v-20zm0 0" fill="#64e1dc"/>
                        <!--TODO: rotation funktioniert noch nicht richtig (2/2) -->
                        <path d="m366 176c0-49.625-40.375-90-90-90h-20c-5.523438 0-10 4.476562-10 10v83.390625c-16.683594-20.613281-42.121094-33.390625-70-33.390625-49.625 0-90 40.375-90 90v20c0 5.523438 4.476562 9.988281 10 9.988281h83.390625c-20.613281 16.6875-33.390625 42.132813-33.390625 70.011719 0 49.625 40.375 90 90 90h20c5.523438 0 10-4.476562 10-10v-83.390625c16.683594 20.613281 42.121094 33.390625 70 33.390625 49.625 0 90-40.375 90-90v-20c0-5.523438-4.476562-10-10-10h-83.390625c20.613281-16.683594 33.390625-42.121094 33.390625-70zm-90-70c38.597656 0 70 31.402344 70 70 0 28.402344-17.035156 53.550781-42.503906 64.390625-5.566406-16.921875-19.910156-29.785156-37.496094-33.375v-101.015625zm-18.097656 179.9375c-16.96875 1.023438-30.847656-11.925781-31.839844-28.035156-1.054688-17.496094 12.804688-31.902344 29.9375-31.902344 16.417969 0 30 13.316406 30 30 0 15.816406-12.351562 28.96875-28.097656 29.9375zm-151.902344-49.9375c0-38.597656 31.402344-70 70-70 28.402344 0 53.550781 17.035156 64.390625 42.503906-16.921875 5.566406-29.785156 19.910156-33.375 37.496094h-101.015625zm130 170c-38.597656 0-70-31.402344-70-70 0-28.402344 17.035156-53.550781 42.503906-64.390625 5.566406 16.921875 19.910156 29.785156 37.496094 33.375v101.015625zm170-130c0 38.597656-31.402344 70-70 70-28.402344 0-53.550781-17.035156-64.390625-42.503906 16.921875-5.566406 29.785156-19.910156 33.375-37.496094h101.015625zm0 0"/>
                    </svg>
                </div>


            </div>
        </header>
        <h3 class="infoMessage">
            {{infoMessage}}
        </h3>

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

                                <!-- Haare normal wenn haar=true && happy = true-->
                                <rect v-if="!this.windStatus" id="Rectangle" transform="translate(211.000000, 70.000000) rotate(38.000000) translate(-211.000000, -70.000000) " x="191" y="19" width="40" height="102" rx="20"></rect>
                                <rect v-if="!this.windStatus" id="Rectangle" transform="translate(152.500000, 66.000000) rotate(27.000000) translate(-152.500000, -66.000000) " x="133" y="2" width="39" height="128" rx="19.5"></rect>
                                <rect v-if="!this.windStatus" id="Rectangle" transform="translate(94.500000, 70.000000) rotate(21.000000) translate(-94.500000, -70.000000) " x="75" y="6" width="39" height="128" rx="19.5"></rect>

                                <!-- Haare Wind -->
                                <path v-if="this.windStatus" :class="{'animate-hair-loosing': !hairStatus }" d="M237.411122,34.5906746 L238.423515,34.7428477 C242.993565,35.4297738 246.141459,39.6913953 245.454533,44.2614459 C245.274318,45.4603983 244.835713,46.6058687 244.169079,47.6185692 L238.147528,56.7660465 L238.147528,56.7660465 L228.561839,77.3456336 L226.328569,105.588574 C225.50606,115.990396 216.825095,124.012024 206.390804,124.012024 L204.871761,124.012024 C196.733309,124.012024 190.13579,117.414505 190.13579,109.276052 C190.13579,107.795738 190.358842,106.323873 190.797435,104.910024 L199.355686,77.321654 L199.355686,77.321654 L210.091995,53.705311 L218.331687,42.5119953 C222.729967,36.5370946 230.074355,33.4878822 237.411122,34.5906746 Z" id="hair3" transform="translate(218.118078, 78.404861) rotate(38.000000) translate(-218.118078, -78.404861) "></path>
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
                            <circle :class="{ 'animate-eyes': happyStatus}" id="Oval" stroke="#979797" fill="#4A4A4A" cx="114" cy="158" r="4"></circle>
                            <circle v-if="!this.eyepokedStatus" :class="{ 'animate-eyes': happyStatus}" id="Oval" stroke="#979797" fill="#4A4A4A" cx="169" cy="158" r="4"></circle>

                            <!-- Mund Traurig -->
                            <path v-if="!this.happyStatus && !this.whistleStatus && !this.windStatus" d="M59,215.333091 C65.0849402,239.631043 100.862006,259 144.08739,259 C187.851338,259 220.584191,239.145382 225.45858,214.422605" id="Path" stroke="#4A4A4A" stroke-width="5" stroke-linecap="round" transform="translate(142.229290, 236.711303) scale(1, -1) translate(-142.229290, -236.711303) "></path>

                            <!-- Mund Happy -->
                            <path v-if="this.happyStatus && !this.whistleStatus && !this.windStatus" d="M56.91261,171.333091 C62.9975502,195.631043 98.7746163,215 142,215 C185.763948,215 218.496801,195.145382 223.37119,170.422605" id="Path" stroke="#4A4A4A" stroke-width="5" stroke-linecap="round"></path>

                            <!-- Mund pfeiffen -->
                            <path  v-if="this.whistleStatus" d="M144,236 C144,230.477153 139.522847,226 134,226" id="whistle" stroke="#4A4A4A" transform="translate(139.000000, 231.000000) rotate(38.000000) translate(-139.000000, -231.000000) "></path>
                            <g :class="{ 'animate-mouth': whistleStatus}" v-if="this.whistleStatus" id="mouth">
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
    import {Howl} from 'howler';
    require('howler');

    export default {
        data:() => ({
            color: '#EDD60C',
            happyStatus: false,
            infoMessage: 'not happy',
            eyepokedStatus: false,
            whistleStatus: false,
            musicStatus: false,
            windStatus: false,
            hairStatus: true
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
                this.playSound('despacito.wav',0.5);
                this.musicStatus = true;
                setTimeout(() => {
                    this.startWhistling();
                }, 2000);
            },
            stopMusic () {
                this.musicStatus = false;
                setTimeout(() => {
                    this.whistleStatus = false;
                    this.happyStatus = true;
                    this.infoMessage = (this.happyStatus ? 'happy' : 'not happy');
                }, 2000);
            },
            startWhistling() {

                setTimeout(() => {
                    this.infoMessage = 'whistling';
                    this.whistleStatus = true;
                    this.playSound('whistle.wav',1);
                }, 400);
                setTimeout(() => {
                    this.stopMusic();
                }, 4500);
            },
            startWind () {
                this.infoMessage = 'wind is blowing';
                this.playSound('fan.wav',1);
                this.windStatus = true;
                // TODO: Ein Haar sollte ausfallen und dann langsam wieder wachsen
                setTimeout(() => {
                    this.hairStatus = false;
                }, 2500);
                setTimeout(() => {

                    this.windStatus = false;
                    this.happyStatus = false;
                    this.infoMessage = (this.happyStatus ? 'happy' : 'not happy');
                }, 5000);
            },
            playSound(filePath, volume) {
                console.log("musik1")
                let sound = new Howl({
                    html5: true,
                    src: filePath,
                    volume: volume
                });
                sound.play();
                console.log("musik")
            }
        }
    }

</script>

<style>
    .animate-hair-loosing {
        position: absolute;
        animation: loosingHair 4s;
    }
    @keyframes loosingHair {
        0%   {      transform: rotateX(0deg)    }
        100% {      transform: translateX(-180px); transform: scale(0.2); opacity: 0 }
    }
    .animate-hair-growing {
        position: absolute;
        animation: growingHair 3s;
    }
    @keyframes growingHair {
        0%      {   transform: translateX(-180px); transform: scale(0.2); opacity: 0 }
        100%    {    transform: rotateX(0deg)    }
    }

    .animate-radio {
        position: absolute;
        animation: radioAnimation 1s infinite;
    }
    @keyframes radioAnimation {
        0%   {    transform: scale(1,1)   }
        50% {   transform: scale(1.2,1.2)   }
        100% {   transform: scale(1,1)   }
    }

    .animate-fan {
        position: absolute;
        animation: fanAnimation 1s infinite;
    }
    @keyframes fanAnimation {
        0%   {    transform: rotate(0deg)   }
        50%   {    transform: rotate(2720deg)   }
        100% {   transform: rotate(0deg)   }
    }

    .animate-eyes{
        position: absolute;
        z-index: 2;
        height: 15%;
        width: 15%;
        top: 1%;
        left:5%;
        animation: lookingAround 4s infinite;
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

    .animate-mouth{
        position: absolute;
        z-index: 2;
        height: 15%;
        width: 15%;
        top: 1%;
        left:5%;
        animation: whistle 0.8s infinite;
    }
    @keyframes whistle {
        0%   {    transform: rotateY(0deg)   }
        100% {   transform: rotateY(-20deg)   }
    }


    .infoMessage {
        position: center;
    }
    .musicButton {
        position: fixed;
        left: 5%;
        top: 3%;

    }
    .windButtonButton {
        position: fixed;
        right: 10%;
        top: 3%;
    }
    .svgCombined {
        position: relative;
    }

</style>
