<template>
    <div class="header">
        <CaptionBox caption="Profession">
            <a href="/Software">Software</a>
            <a href="/Websites">Websites</a>
        </CaptionBox>

        <button>GET IN TOUCH</button>

        <CaptionBox caption="Hobby">
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
}

.header {
    position: fixed;
    top: 0;
    left: 0;
    width: 100%;
    height: 60px;
    display: flex;
    justify-content: space-evenly;
    font-weight: bold;
    padding-bottom: 10px;
    padding-top: 5px;
    background-color: $quad-color;
    align-items: center;
}
</style>