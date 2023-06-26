<template>
    <div class="header">
        <CaptionBox caption="Profession">
            <a href="/Software">Software</a>
            <a href="/Software">Games</a>
            <a href="/Websites">Websites</a>
        </CaptionBox>

        <button>GET IN TOUCH</button>

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
button {
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
}

.header {
    position: fixed;
    top: 0;
    left: 0;
    width: 100vw;
    background-color: $quad-color;
    padding-bottom: 10px;
    padding-top: 5px;
}

.hobby {
    display: none;
}

@media only screen and (min-width: 1200px) {
    button {
        display: block;
    }

    .header {
        height: 60px;
        display: flex;
        justify-content: space-evenly;
        font-weight: bold;
        align-items: center;
    }

    .hobby {
        display: block;
    }
}
</style>