<template>
    <div class="statblock">
        <div class="stat">{{ stat }}</div>
        <div class="desc">{{ desc }}</div>
    </div>
</template>

<script>
export default {
    name: 'StatBlock',
    props: {
        stat: {
            type: String,
            default: '00',    
        },
        desc: {
            type: String,
            default: 'Description'
        }
    }
}
</script>

<style lang="scss">
.statblock {
    scroll-snap-align: start;

    .stat {
        color: $primary-color;
        font-size: 3rem;
        font-weight: bold;
    }

    .desc {
        color: $tertiary-color;
        font-size: 2rem;
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