<template>
    <label class="project">
        <input type="checkbox">
        <div class="background" :style="{'background-image': `url(${image})`}"/>
        <div class="project_content">
            <h1 class="title">{{ title  }}</h1>
            <div class="desc">{{ desc }}</div>
            <a v-if="link" class="ref" :href="link" target="_blank">{{ linkTitle }}</a>
            <div class="tags">
                <span
                    class="tag"
                    v-for="tag in tags" 
                    :key="tag">
                    {{ tag }}
                </span>
            </div>
        </div>
    </label>
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
        linkTitle: {
            type: String,
            default: 'VIEW ON GITHUB'
        },
        link: {
            type: String,
            default: ''
        },
        image: {
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
    max-height: 300px;
    min-height: 200px;
    width: 400px;
    max-width: 100vw;
    border-radius: 10px;
    display: flex;
    flex-direction: column;
    justify-content: flex-end;
    overflow:hidden;
    position: relative;
    margin: 10px;

    cursor: pointer;

    input[type="checkbox"] {
        position: absolute;
        opacity: 0;
        cursor: pointer;
        height: 0;
        width: 0;
    }

    input[type="checkbox"]:not(:checked) ~ .project_content>.desc, 
    input[type="checkbox"]:not(:checked) ~ .project_content>.ref
    {
        display: none;
    }

    input[type="checkbox"]:not(:checked) ~ .background
    {
        filter: none;
        -webkit-filter: none;
    }

    :checked {
        border: 1px solid salmon;
    }

    .background {
        height: 100%;
        width: 100%;
        position: absolute;
        background-position-y: center;
        background-size: cover;
        background-repeat: no-repeat;
        z-index: 0;
        filter: blur(6px);
        -webkit-filter: blur(6px);
        box-shadow: inset 0px 0px 20px 8px $quad-color;
    }

    .project_content {
        display: flex;
        flex-direction: column;
        align-items: center;
        justify-content: space-between;
        justify-content: flex-end;
        background-color: $primary-color;
        z-index: 1;
        width: 100%;
        gap: 10px;

        .title, .desc {
            z-index: 1;
            color: $quad-color;
        }

        .ref {
            width: 150px;
            background-color: $quad-color;
            border-radius: 10px;
            height: 50px;
            display: flex;
            justify-content: center;
            align-items: center;
            color: $quad-color;
            font-weight: bold;
            z-index: 1;
            color: $secondary-color;
        }

        .tags {
            display: flex;
            width: 400px;
            max-width: 100vw;
            justify-content: space-evenly;
            gap: 10px;
            flex-wrap: wrap;
            z-index: 1;
            
            .tag {
                background-color: $tertiary-color;
                text-shadow: 2px 0 $quad-color, -2px 0 $quad-color, 0 2px $quad-color, 0 -2px $quad-color,
                1px 1px $quad-color, -1px -1px $quad-color, 1px -1px $quad-color, -1px 1px $quad-color;
                box-shadow: 0px 0px 5px 0px rgba(0,0,0,1);
                -webkit-box-shadow: 0px 0px 5px 0px rgba(0,0,0,1);
                -moz-box-shadow: 0px 0px 5px 0px rgba(0,0,0,1);
                box-shadow: 1px 1px 1px 1px solid;
                border-radius: 5px;
                width: unset;
                padding: 3px;
                bottom: 0px;
            }
        }
    }
}

@media only screen and (min-width: 1200px) {
    .project {
    height: 300px;
    width: 500px;
    border-radius: 10px;
    display: flex;
    flex-direction: column;
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