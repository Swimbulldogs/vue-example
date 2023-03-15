<script>
import NavBar from './NavBar.vue'

export default {
    data() {
        const otherDogs= [
                {
                    src: "https://images.squarespace-cdn.com/content/v1/5dd8630d09ab5908e35b35a0/1574462664001-48S1VO61L9LNWNJ910CV/img-HotDogStock-1080x675.png?format=1000w",
                    hotdog: "default"
                },
                {
                    src: "https://www.agefotostock.com/age/en/details-photo/hot-dog-with-relish-onion-ketchup-mustard/SFD-12991405",
                    hotdog: "relish"
                },
                {
                    src: "https://www.pinterest.com/pin/761038037015424106/",
                    hotdog: "whipped cream"
                },
                {
                    src: "https://juliassimplysouthern.com/2014/05/julias-southern-hot-dog-chili-1.html",
                    hotdog: "meat on hotdog"
                },
                {
                    src: "https://www.seriouseats.com/grilled-hot-dogs-with-sauerkraut-recipe",
                    hotdog: "sauerkraut"
                },
                {
                    src: "https://www.thrillist.com/eat/nation/ketchup-on-hot-dogs-best-toppings",
                    hotdog: "ketchup"
                },
                {
                    src: "https://www.foodnetwork.com/recipes/bobby-flay/grilled-link-hot-dogs-with-homemade-pickle-relish-recipe-1942988",
                    hotdog: "pickles"
                }
            ];
            const res = otherDogs.find(x => x.hotdog == this.hotdog);
            console.log(res);
        return {
            hotdog: this.hotdog,
            src: res.src,
            otherDogs: otherDogs,
        }
    },
    emits: ['changeData'],
    methods: {
        changeData(hotdog) {
            this.src = hotdog.src;
            this.$emit('changeData', hotdog.hotdog);
        }
    },
    props: {
        hotdog: String
    },
    components: { NavBar },
}
</script>

<template>
    <body>
        <NavBar></NavBar>
        <img :src="src" alt="hotdog">
        <div class="links">
            <!-- do you think you could wrap this better?-->
            <a v-on:click="e => changeData(otherDogs[1])">
                Put some {{ otherDogs[1].hotdog }} on it
            </a>

            <a v-on:click="e => changeData(otherDogs[2])">
                Put some {{ otherDogs[2].hotdog }} on it
            </a>

            <a v-on:click="e => changeData(otherDogs[3])">
                Put some {{ otherDogs[3].hotdog }} on it
            </a>
            <a v-on:click="e => changeData(otherDogs[4])">
                Put some {{ otherDogs[4].hotdog }} on it
            </a>
            <a v-on:click="e => changeData(otherDogs[5])">
                Put some {{ otherDogs[5].hotdog }} on it
            </a>
            <a v-on:click="e => changeData(otherDogs[6])">
                Put some {{ otherDogs[6].hotdog }} on it
            </a>

        </div>
    </body>
</template>

<style scoped>
img {
    display: block;
    margin-left: auto;
    margin-right: auto;
}

.links {
    display: flex;
    justify-content: space-evenly;
}
</style>
