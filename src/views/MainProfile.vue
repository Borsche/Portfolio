<template>
    <div class="mainprofile">
        <div class="text">
            <span>Welcome,</span><br>
            <span class="plus">my name is <span class="bold">Blazej Josko</span> and</span><br>
            <span class="big bold">I am a Software Developer<span class="blink">|</span></span><br>
            <span>Currently I am a Full Stack Developer at OSP</span><br>
            <span>Where I develop and maintain Frontend and Backend Services for the Resy Team</span><br>
            <a class="download" href="../assets/CV2023EnglishBlazejJosko.pdf" download>Download CV</a><a href="https://github.com/Borsche/">My Github Page</a>
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

    a, .download {
        background-color: $primary-color; 
        border-radius: 3px;
        border: none;
        font-size: 1rem;
        font-weight: bold;
        margin: 5px;
        padding: 5px;
        color: $quad-color;
        height: 50px;
        cursor: pointer;
        max-width: 150px;
    }
    
    a {
        background-color: $tertiary-color;
        color: $secondary-color;
        display: flex;
        justify-content: center;
        align-items: center;
        width: fit-content;
    }

    .download {
        display: none;
    }

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