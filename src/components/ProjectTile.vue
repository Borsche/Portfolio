<template>
    <div class="project">
        <h1>{{ title  }}</h1>
        <div>{{ desc }}</div>
        <a class="ref" :href="link">VIEW ON GITHUB</a>
        <div class="tags">
            <span
                class="tag"
                v-for="tag in tags" 
                :key="tag">
                {{ tag }}
            </span>
        </div>
    </div>
</template>
<script>
export default {
    name: 'ProjectTile',
    props: {
        title: {
            type: String,
            default: 'Project',    
        },
        desc: {
            type: String,
            default: 'Description'
        },
        link: {
            type: String,
            default: ''
        },
        tags: {
            type: Array,
            default: () => []
        }
    }
}
</script>

<style lang="scss">
.project {
    height: 300px;
    width: 400px;
    max-width: 100vw;
    border-radius: 10px;
    display: flex;
    flex-direction: column;
    justify-content: space-evenly;
    position: relative;
    align-items: center;

    .ref {
        width: 150px;
        background-color: $primary-color;
        border-radius: 10px;
        height: 50px;
        display: flex;
        justify-content: center;
        align-items: center;
        color: $quad-color;
        font-weight: bold;
    }

    .tags {
        display: flex;
        width: 400px;
        max-width: 100vw;
        justify-content: space-evenly;
        gap: 10px;
        flex-wrap: wrap;
        
        .tag {
            background-color: $tertiary-color;
            border-radius: 5px;
            width: unset;
            padding: 3px;
            bottom: 0px;
        }
    }
}

@media only screen and (min-width: 1200px) {
    .project {
    height: 300px;
    width: 500px;
    border: 1px solid salmon;
    border-radius: 10px;
    display: flex;
    flex-direction: column;
    justify-content: space-evenly;
    position: relative;
    align-items: center;

    .ref {
        width: 150px;
        background-color: $primary-color;
        border-radius: 10px;
        height: 50px;
        display: flex;
        justify-content: center;
        align-items: center;
        color: $quad-color;
        font-weight: bold;
    }

    .tags {
        display: flex;
        width: 500px;
        justify-content: space-evenly;
        gap: 10px;
        flex-wrap: wrap;
        
        .tag {
            background-color: $tertiary-color;
            border-radius: 5px;
            width: unset;
            padding: 3px;
            bottom: 0px;
        }
    }
}
}
</style>