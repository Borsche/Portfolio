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
    border: 1px solid $tertiary-color;
    border-radius: 15px;
    text-align: center;
    font-size: 1rem;
    padding: 5px 0px 5px 0;
    display: flex;
    justify-content: space-around;
    align-items: center;
    background-color: $tertiary-color;
}

.captionbox {
    text-align: left;
    flex-direction: column;
    font-weight: bold;
    font-size: .8rem;
    color: $tertiary-color;
}

@media only screen and (min-width: 1200px) {
    .captionboxcontent {
        height: 50px;
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
}
</style>