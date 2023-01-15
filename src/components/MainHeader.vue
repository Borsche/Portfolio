<template>
    <div class="header">
        <CaptionBox caption="Profession">
            <a href="/Software">Software</a>
            <a href="/Websites">Websites</a>
        </CaptionBox>

        <button>Get in touch</button>

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

<style>
button {
    background-color: rgb(7, 126, 52);
    border: none;
}

.header {
    position: fixed;
    width: 100%;
    height: 60px;
    display: flex;
    justify-content: space-evenly;
    font-weight: bold;
}
</style>