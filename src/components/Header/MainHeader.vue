<template>
    <div class="header">
        <CaptionBox caption="Profession">
            <a href="#Software">Software</a>
            <a href="#Games">Games</a>
            <a href="#Websites">Websites</a>
        </CaptionBox>

        <a class="contact" href="mailto:blazejjosko@hotmail.de">GET IN TOUCH</a>

        <CaptionBox caption="Hobby" class="hobby">
            <a href="/modeling" >3D Modeling</a>
            <a href="/modeling" >Photography</a>
        </CaptionBox>
    </div>
</template>

<script>
import CaptionBox from './CaptionBox.vue';

export default {
    name: 'MainHeader',
    components: {
        CaptionBox
    }
}
</script>

<style lang="scss">
.header {
    position: fixed;
    top: 0;
    left: 0;
    width: 100vw;
    background-color: $quad-color;
    padding-bottom: 10px;
    padding-top: 5px;
    z-index: 10;
    
    .hobby {
        display: none;
    }

    .contact {
        background-color: $primary-color; 
        border-radius: 3px;
        border: none;
        font-size: 1rem;
        font-weight: bold;
        margin: 5px;
        padding: 5px;
        color: $quad-color;
        height: 50px;
        display: none;
        cursor: pointer;
    }
}

@media only screen and (min-width: 1200px) {
   .header {
        height: 60px;
        display: flex;
        justify-content: space-evenly;
        font-weight: bold;
        align-items: center;

        .contact {
            display: flex;
            justify-content: center;
            align-items: center;
        }
        .hobby {
            display: none;
        }
    }
}
</style>