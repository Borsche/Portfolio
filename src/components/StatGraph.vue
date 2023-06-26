<template>
    <div class="statgraph">
        <div class="stat">{{ stat }}</div>
        <div class="statgraphlimiter">
            <div class="desc" :style="{width: width+'%'}"></div>
        </div>
        <div class="desctext">{{ desc }}</div>
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
    min-width: 50px;
    max-width: 1200px;
    display: flex;
    align-items: center;
    justify-content: flex-end;

    .stat {
        color: $primary-color;
        max-width: 10px;
        font-size: 2rem;
        font-weight: bold;
        z-index: 1;
    }

    .statgraphlimiter {
        width: 70vw;
    }

    .desc {
        color: $secondary-color;
        font-size: 1rem;
        background-color: $tertiary-color;
        height: 20px;
        display: flex;
        align-items: center;
        justify-content: center;
        white-space: nowrap;
        padding-bottom: 10px;
    }

    .desctext {
        color: $primary-color;
        font-weight: 500;
    }
}

@media only screen and (min-width: 1200px) {
    .statgraph {
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
}

</style>