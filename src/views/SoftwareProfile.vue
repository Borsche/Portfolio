<template>
    <ProjectsProfile
        sectionId="Software"
        desc="Here is a collection of a few projects which are publicly available on my Github Account. All of these projects where done by me. By clicking on a project you can open a description to read more about the project. In addition to that a button will show up which redirects you to the Github Repository."
    >
        <ProjectTile
            title="TS3-Monitoring Bot"
            desc="A bot which reacts to specified commands send through teamspeak to allow for a simple monitoring."
            link="https://github.com/Borsche/teamspeak-monitoring-bot"
            :tags="['Node.js', 'Typescript', 'API', 'Teamspeak3']"
            :image="require('@/assets/projects/Teamspeak.png')"
        />
        <ProjectTile
            title="Twitch Voting Tool"
            desc="A tool for twitch which allows the streamer to set up quick Polls. The viewers can then vote through the chat. Trough customizable shortcuts the Streamer can work more efficiently."
            link="https://github.com/Borsche/Twitch-VoteCounter"
            :tags="['Node.js', 'Typescript', 'Electron', 'API', 'Twitch']"
            :image="require('@/assets/projects/TwitchVoting.png')"
        />
        <ProjectTile
            title="Loyalty Twitch"
            desc="A huge WIP Project. A software which allows the viewers to earn points by watching the stream and playing minigames with others. These points can then be spend on by the streamer defined commands. The old Java Codebase is currently being redone in Node.js."
            link="https://github.com/Borsche/Loyalty_Backend"
            :tags="['Node.js', 'Typescript', 'PostgreSQL', 'API', 'Twitch', 'Java', 'SpringBoot', 'Vue.js']"
            :image="require('@/assets/projects/Loyalty.png')"
        />
        <ProjectTile
            title="Twitch TTS"
            desc="A simple tts service which runs locally on the streamers pc and reads out chat message."
            link="https://github.com/Borsche/TTS-TwitchChat"
            :tags="['Node.js', 'Javascript', 'API', 'Twitch',]"
            :image="require('@/assets/projects/TTS.png')"
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