<template>
    <div class="softwareprofile">
        <h1 id="softwareCategory" class="category">Software</h1>
        <ProjectTile
            title="TS3-Monitoring Bot"
            desc="A bot which reacts to specified commands send through teamspeak to allow for a simple monitoring."
            link="https://github.com/Borsche/teamspeak-monitoring-bot"
            :tags="['Node.js', 'Typescript', 'API', 'Teamspeak3']"
        />
        <ProjectTile
            title="Twitch Voting Tool"
            desc="A tool for twitch which allows the streamer to set up quick Polls. The viewers can then vote through the chat. Trough customizable shortcuts the Streamer can work more efficiently."
            link="https://github.com/Borsche/teamspeak-monitoring-bot"
            :tags="['Node.js', 'Typescript', 'Electron', 'API', 'Twitch']"
        />
        <ProjectTile
            title="Loyalty Twitch"
            desc="A huge WIP Project. A software which allows the viewers to earn points by watching the stream and playing minigames with others. These points can then be spend on by the streamer defined commands. The old Java Codebase is currently being redone in Node.js."
            link="https://github.com/Borsche/teamspeak-monitoring-bot"
            :tags="['Node.js', 'Typescript', 'PostgreSQL', 'API', 'Twitch', 'Java', 'SpringBoot', 'Vue.js']"
        />
    </div>
</template>

<script>
import ProjectTile from './ProjectTile.vue'

export default {
    name: 'SoftwareProfile',
    components: {
        ProjectTile,
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

    .category {
        width: 100vw;
    }
}

@media only screen and (min-width: 1200px) {
    .statblock {

        .stat {
            font-size: 8rem;
        }

        .desc {
            color: $tertiary-color;
            font-size: 2rem;
        }
    }
}

</style>