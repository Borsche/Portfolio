<template>
    <ProjectsProfile
        sectionId="Games"
        desc="I have a lot of games/ideas under development. Most of them are done in Unity. If a game reaches an MVP state it will try to make it publicly available and put it here."
    >
        <ProjectTile
            title="Space Bullet Hell"
            desc="A sidescroller game from the bullet hell genre where the player controls a ship in space and tries to dodge the enemy while destroying them to get to the final boss of each level."
            :tags="['Unity', '2D', 'Self Made Assets']"
            :image="require('@/assets/games/SpaceBulletHell.png')"
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