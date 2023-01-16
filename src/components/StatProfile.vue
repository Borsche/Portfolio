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
                desc="7+ years"
                width="100"
            />
            <StatGraph
                stat="C#"
                desc="7+ years"
                width="100"
            /> 
            <StatGraph
                stat="Node.js"
                desc="4+ years"
                width="57"
            /> 
            <StatGraph
                stat="Vue"
                desc="2+ years"
                width="28.5"
            /> 
            <StatGraph
                stat="GoLang"
                desc="1+ year"
                width="14"
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