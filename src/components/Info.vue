<template>
    <div>
        <!--    Typer JS Text -->
        <h2>
            Hi, <br>
            <span class="typer" id="first-typer" data-words="play some sound, poke me in my right eye, turn on the fan, put me to sleep" data-colors="#cd2032,#cc1e81,#6e6abb"></span>
            <span class="cursor" data-owner="first-typer"></span>
        </h2>
    </div>
</template>

<script>
    export default {
        created() {
            let typer = document.createElement('script');    typer.setAttribute('src',"https://unpkg.com/typer-dot-js@0.1.0/typer.js");
            document.head.appendChild(typer);
        }
    }
</script>
