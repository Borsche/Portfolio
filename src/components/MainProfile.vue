<template>
    <div class="mainprofile">
        <div class="text">
            <span>Welcome,</span><br>
            <span class="plus">my name is <span class="bold">Blazej Josko</span> and</span><br>
            <span class="big bold">I am a Software Developer<span class="blink">|</span></span><br>
            <span>Currently I am a Full Stack Developer at OSP</span><br>
            <span>Where I develop and maintain Frontend and Backend Services for the Resy Team</span><br>
            <button>Download CV</button><button id="projects">Projects</button>
        </div>
        <div class="img"></div>
    </div>
</template>

<script>
export default {
    name: 'MainProfile'
}
</script>

<style lang="scss">
@keyframes blink {
    0% { color: $secondary-color }
    50% { color: $secondary-color }
    51% { color: transparent }
    100% { color: transparent }
}

.mainprofile {
    width: 100%;
    height: 100vh;
    background: linear-gradient(90deg, $quad-color 75%, $primary-color 60%);
    display: flex;
    justify-content: space-evenly;
    align-items: center;
    scroll-snap-align: start;

    .text {
        text-align: left;

        .plus {
            font-size: 1rem;
        }

        .big {
            font-size: 2rem;
            line-height: 3rem;
        }

        .bold {
            font-weight: bold;
        }

        .blink {
            animation-name: blink;
            animation-duration: 1s;
            animation-iteration-count: infinite;
        }

        #projects {
            background-color: $tertiary-color;
            color: $secondary-color;
        }
    }
    
    .img {
        background: url('../assets/Bild.jpg') no-repeat center;
        background-size: cover;
        height: 300*.8px;
        width: 223*1.4px;
        border: 3px solid $primary-color;
        border-radius: 15px;
    }
}

@media only screen and (min-width: 1200px) {
    .mainprofile {
        .text {

            .plus {
                font-size: 1.2rem;
            }

            .big {
                font-size: 3rem;
                line-height: 5rem;
            }
        }

        .img {
            background: url('../assets/Bild.jpg') no-repeat center;
            background-size: cover;
            height: 300*1.4px;
            width: 223*1.4px;
            border: 3px solid $primary-color;
            border-radius: 15px;
        }
    }
}
</style>