<template>
    <div class="statgraph">
        <div class="stat">{{ stat }}</div>
        <div class="statgraphlimiter">
            <div class="desc" :style="{width: width+'%'}">{{ desc }}</div>
        </div>
    </div>
</template>

<script>
export default {
    name: 'StatGraph',
    props: {
        stat: {
            type: String,
            default: '00',    
        },
        desc: {
            type: String,
            default: 'Description'
        },
        width: {
            type: Number,
            default: 100
        }
    }
}
</script>

<style lang="scss">
.statgraph {
    width: 1200px;
    display: flex;
    align-items: center;
    justify-content: flex-end;

    .stat {
        color: $primary-color;
        font-size: 8rem;
        font-weight: bold;
    }

    .statgraphlimiter {
        width: 700px;
    }

    .desc {
        color: $secondary-color;
        font-size: 2rem;
        background-color: $tertiary-color;
        height: 60px;
        display: flex;
        align-items: center;
        justify-content: center;
        white-space: nowrap;
    }
}
</style>