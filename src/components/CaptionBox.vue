<template>
    <div class="captionbox">
        {{caption}}
        <div class="captionboxcontent">
            <slot/>
        </div>
    </div>
</template>

<script>
export default {
    name: 'CaptionBox',
    props: {
        caption: {
            type: String,
            default: 'Caption'
        }
    }
}
</script>

<style lang="scss">
.captionboxcontent {
    border: 3px solid $tertiary-color;
    border-radius: 15px;
    text-align: center;
    font-size: 1rem;
    height: 50px;
    display: flex;
    justify-content: space-around;
    align-items: center;
    background-color: $primary-color;
    background-blend-mode: lighten;
}

.captionbox {
    width: 400px;
    text-align: left;
    display: flex;
    flex-direction: column;
    font-weight: bold;
    font-size: .8rem;
    color: $tertiary-color;
}
</style>