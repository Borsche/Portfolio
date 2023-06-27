<template>
    <div class="profile">
        <h1 :id="sectionId" class="category">{{ sectionId }}</h1>
        <div class="descContainer">    
            <span class="desc">{{ desc }}</span>
        </div>
        <slot/>
    </div>
</template>

<script>
export default {
    name: 'ProjectsProfile',
    props: {
        sectionId: {
            type: String,
            default: '',
        },
        desc: {
            type: String,
            default: '',
        }
    }
}
</script>

<style lang="scss">
.profile {
    background-color: $quad-color;
    scroll-snap-align: start;

    display: flex;
    flex-wrap: wrap;
    align-content: space-around;
    flex-direction: row;
    justify-content: space-evenly;
    gap: 50px;

    padding-top: 50px;

    .category {
        font-size: 3rem;
        color: $primary-color;
        width: 100vw;
    }

    .descContainer {
        width: 100%;
        display: flex;
        justify-content: center;

        .desc {
            max-width: 800px;
            word-wrap: normal;
            display: block;
        }
    }
}

@media only screen and (min-width: 1200px) {
    .profile {
        height: 100vh;
        padding-top: 0;

        .category {
            font-size: 8rem;
        }
    }
}

</style>