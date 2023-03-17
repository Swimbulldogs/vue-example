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
                    src: "https://previews.agefotostock.com/previewimage/medibigoff/675a51f9f102310bc61c0ec4ec9e40b6/sfd-12991405.jpg",
                    hotdog: "relish"
                },
                {
                    src: "https://complex-res.cloudinary.com/image/upload/rhcvsg8mhkqdichmwew9.jpg",
                    hotdog: "whipped cream"
                },
                {
                    src: "https://flyingcdn-cf8480cb.b-cdn.net//wp-content/uploads/2022/01/Chili-Dogs-on-a-Platter.jpg?width=800",
                    hotdog: "chilli on hotdog"
                },
                {
                    src: "https://www.seriouseats.com/thmb/s6XumFs3Fe4Otd8NejuSXzIVMKU=/1500x0/filters:no_upscale():max_bytes(150000):strip_icc()/__opt__aboutcom__coeus__resources__content_migration__serious_eats__seriouseats.com__recipes__images__2012__05__20120529-food-lab-cooking-sausage-hot-dog-19-e55675e3468b4189a38392ece9d77d4d.jpg",
                    hotdog: "sauerkraut"
                },
                {
                    src: "https://assets3.thrillist.com/v1/image/2810448/1584x1056/crop;jpeg_quality=60;progressive.jpg",
                    hotdog: "ketchup"
                },
                {
                    src: "https://food.fnr.sndimg.com/content/dam/images/food/fullset/2010/4/13/0/GC_hot-dog-with-pickle-relish_s4x3.jpg.rend.hgtvcom.1280.720.suffix/1371592835029.jpeg",
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
