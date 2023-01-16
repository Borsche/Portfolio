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

    .stat {
        color: $primary-color;
        font-size: 8rem;
        font-weight: bold;
    }

    .desc {
        color: $tertiary-color;
        font-size: 2rem;
    }
}
</style>