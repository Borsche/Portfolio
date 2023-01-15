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

<style scoped>
.captionboxcontent {
    border: 1px solid rgb(7, 126, 52);
    border-radius: 15px;
    text-align: center;
    font-size: 1rem;
    height: 50px;
    display: flex;
    justify-content: space-around;
    align-items: center;
    background-color: rgb(7, 126, 52, 25%);
}

a {
    color: black;
}

.captionbox {
    width: 400px;
    text-align: left;
    display: flex;
    flex-direction: column;
    color: rgb(7, 126, 52);
    font-weight: bold;
}

.captionbox:hover {
    font-size: .8rem;
}
</style>