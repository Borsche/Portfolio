<template>
    <div class="statprofile">
        <StatBlock
            stat="6+"
            desc="years of working experience"
        />
        <div class="statlist">
            <span class="">Experienced in</span> 
            <StatGraph
                stat="Java"
            />
            <StatGraph
                stat="C#"
            />
            <StatGraph
                stat="Unity"
            />  
            <StatGraph
                stat="Node.js"
            /> 
            <StatGraph
                stat="TypeScript"
            /> 
            <StatGraph
                stat="Javascript"
            /> 
            <StatGraph
                stat="Vue"
            /> 
            <StatGraph
                stat="GoLang"
            /> 
        </div>
    </div>
</template>

<script>
import StatBlock from './StatBlock.vue'
import StatGraph from './StatGraph.vue'

export default {
    name: 'StatProfile',
    components: {
        StatBlock,
        StatGraph
    }
}
</script>

<style lang="scss">
.statprofile {
    height: 100vh;
    background-color: $quad-color;
    width: 100%;
    display: flex;
    flex-direction: column;
    justify-content: space-evenly;
    scroll-snap-align: start;
    .statlist {
        display: flex;
        flex-direction: column;
        align-items: center;

        span {
            color: $tertiary-color;
            font-size: 2rem;
        }
    }
}
</style>