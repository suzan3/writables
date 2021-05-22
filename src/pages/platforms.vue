<template>
<q-page class="bg px-10 q-pt-xl">
    <div class="row">
        <div class="col-12 text-center">
            <p class="title"> PLATFORMS </p>
        </div>
        <div class="col-md-9 col-12 q-mx-auto text-center">
            <p class="description"> See anything that interests you? Click on any of the platforms to subscribe!
                For more infromation on what the platforms offer, please <span class="click">click here.</span> </p>
        </div>
    </div>
    <div class="row q-mt-xl q-px-xxl">
        <div v-for='index in ListOfPlatforms' :key='index' class="col-md-3 col-sm-6 col-12 text-center">
            <img :src="index.src" width="60%" class="q-mb-lg">
        </div>
    </div>
    <div class="line q-mx-auto q-my-xl">
    </div>
    <div class="row">
        <div v-for='index1 in 12' :key='index1' class="col-md-3 col-sm-6 col-12 text-center">
            <q-img src="~assets/image.png" width="60%" class="img q-my-lg">
                <div class="absolute-full text-subtitle2 flex flex-center d-hover q-my-auto">
                    TITLE
                </div>
            </q-img>
        </div>
    </div>
</q-page>
</template>

<style>
.d-hover {
    display: none;
    font-size: 30px;
}

.img:hover div.d-hover {
    display: flex;
    align-items: center;
    justify-content: center;
    cursor: pointer;
}



.title {
    border-bottom: 2px solid #BC8037;
    font-size: 48px;
    font-family: 'AGENCYR';
}

.px-10 {
    padding-left: 10%;
    padding-right: 10%;
}

.description {
    font-size: 24px;
    font-family: 'HelveticaNeueLTStd-Roman';
}

.click {
    color: #BC8037;
    border-bottom: 2px solid #BC8037;
    cursor: pointer;
}

.line {
    background-color: #BC8037;
    width: 60%;
    height: 2px;
}

.q-px-xxl {
    padding-left: 65px;
    padding-right: 65px;
}
</style>

<script>
const images = [{
        src: require("assets/platforms/books.png")
    },
    {
        src: require("assets/platforms/games.png")
    },
    {
        src: require("assets/platforms/movies.png")
    },
    {
        src: require("assets/platforms/plays.png")
    },
    {
        src: require("assets/platforms/poems.png")
    },
    {
        src: require("assets/platforms/series.png")
    },
    {
        src: require("assets/platforms/songs.png")
    },
    {
        src: require("assets/platforms/stories.png")
    },

];
export default {
    name: 'platforms',
    data() {
        return {
            ListOfPlatforms: images,
        }
    }
}
</script>
