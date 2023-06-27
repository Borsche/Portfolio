<template>
    <ProjectsProfile
        sectionId="Websites"
        desc="This list is currently under development. But this is the current list of all available websites I've created over the years. All of these website have been done by me."
    >
        <ProjectTile
            title="Portfolio"
            desc="The website you are currently on. Click the button to see the source code!"
            link="https://github.com/Borsche/Portfolio"
            :tags="['Vue3', 'Responsive', 'CI/CD Pipeline']"
            :image="require('@/assets/websites/Portfolio.png')"
        />
        <ProjectTile
            title="Loyalty Twitch"
            desc="The website for the loyalty twitch software described at the software section. This site is currently not publicly available but you can have a look at the current state of the source code!"
            link="https://github.com/Borsche/Loyalty_Frontend"
            :tags="['Vue3', 'Vite']"
            :image="require('@/assets/projects/Loyalty.png')"
        />
    </ProjectsProfile>
</template>

<script>
import ProjectTile from '@/components/Project/ProjectTile.vue'
import ProjectsProfile from '@/components/Project/ProjectsProfile.vue'

export default {
    name: 'SoftwareProfile',
    components: {
        ProjectTile,
        ProjectsProfile,
    }
}
</script>

<style lang="scss">
.softwareprofile {
    background-color: $quad-color;
    scroll-snap-align: start;

    display: flex;
    flex-wrap: wrap;
    align-content: space-around;
    flex-direction: row;
    justify-content: space-evenly;
    gap: 50px;

    #softwareCategory {
        font-size: 3rem;
        color: $primary-color;
    }

    .softwareDescContainer {
        width: 100%;
        display: flex;
        justify-content: center;

        .softwareDesc {
            max-width: 800px;
            word-wrap: normal;
            display: block;
        }
    }

    .category {
        width: 100vw;
    }
}

@media only screen and (min-width: 1200px) {
    .softwareprofile {
        height: 100vh;

        #softwareCategory {
            font-size: 8rem;
        }
    }
}

</style>