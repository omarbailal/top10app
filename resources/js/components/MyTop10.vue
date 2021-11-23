<template>
    <div class="">
        <h1 class="text-lg md:text-xl text-gray-800 font-semibold my-2 ml-12">{{top10Titles[x]}}</h1>
        <div class="flex items-center">
            <button @click="changeLeft" class="mr-1 -ml-1 text-gray-700  hover:bg-gray-300 px-3 py-1  rounded-full focus:outline-none">
                <i class="fas fa-angle-left fa-2x "></i>
            </button>
            <div id="scroll" style="height:440px" class="bg-white border rounded-md w-full overflow-y-auto ">
                <div class="flex flex-col mx-2 ">
                    <div v-for="item in currentTop10(x)" v-bind:key="item" class="flex items-center justify-between border-b-2 my-2 ">
                    <mytop10item v-bind:item= "item" />
                    </div>
                </div>
            </div>
            <button @click="changeRight" class="ml-1 -mr-1 text-gray-700  hover:bg-gray-300 px-3 py-1 rounded-full focus:outline-none">
                <i class="fas fa-angle-right fa-2x "></i>
            </button>
        </div>
    </div>
</template>

<script>
    import mytop10item from './MyTop10Item';
    export default {
        components: {
            mytop10item,
        },
        methods: {
            currentTop10(x){
                if(x == 0)
                return this.top10s.movies;
                if(x == 1)
                return this.top10s.tvshows;
                if(x == 2)
                return this.top10s.anime;
            },
            changeLeft(){
                this.x == 0 ? this.x = 2 : this.x--;
            },
            changeRight(){
                this.x == 2 ? this.x = 0 : this.x++;
            },

        },
        data(){
            return {
                top10Titles: ["top10 Movies", "top10 Tvshows", "top10 Anime"],
                x: 0,
                top10s: {
                   movies: [
                        {
                            id: 1,
                            title: 'The Man from Earth',
                            img: 'https://upload.wikimedia.org/wikipedia/en/3/3b/The_Man_from_Earth.png',
                            desc: 'Sci-fi/Indie film ‧ 1h 30m',
                            up: 0,
                            down: 0,
                        },
                        {
                            id: 2,
                            title: 'The Man from Earth',
                            img: 'https://upload.wikimedia.org/wikipedia/en/3/3b/The_Man_from_Earth.png',
                            desc: 'Sci-fi/Indie film ‧ 1h 30m',
                            up: 0,
                            down: 0,
                        },
                        {
                            id: 3,
                            title: 'The Man from Earth',
                            img: 'https://upload.wikimedia.org/wikipedia/en/3/3b/The_Man_from_Earth.png',
                            desc: 'Sci-fi/Indie film ‧ 1h 30m',
                            up: 0,
                            down: 0,
                        },
                        {
                            id: 4,
                            title: 'The Man from Earth',
                            img: 'https://upload.wikimedia.org/wikipedia/en/3/3b/The_Man_from_Earth.png',
                            desc: 'Sci-fi/Indie film ‧ 1h 30m',
                            up: 0,
                            down: 0,
                        },
                        {
                            id: 5,
                            title: 'The Man from Earth',
                            img: 'https://upload.wikimedia.org/wikipedia/en/3/3b/The_Man_from_Earth.png',
                            desc: 'Sci-fi/Indie film ‧ 1h 30m',
                            up: 0,
                            down: 0,
                        },
                        {
                            id: 6,
                            title: 'The Man from Earth',
                            img: 'https://upload.wikimedia.org/wikipedia/en/3/3b/The_Man_from_Earth.png',
                            desc: 'Sci-fi/Indie film ‧ 1h 30m',
                            up: 0,
                            down: 0,
                        },
                        {
                            id: 7,
                            title: 'The Man from Earth',
                            img: 'https://upload.wikimedia.org/wikipedia/en/3/3b/The_Man_from_Earth.png',
                            desc: 'Sci-fi/Indie film ‧ 1h 30m',
                            up: 0,
                            down: 0,
                        },
                        {
                            id: 8,
                            title: 'The Man from Earth',
                            img: 'https://upload.wikimedia.org/wikipedia/en/3/3b/The_Man_from_Earth.png',
                            desc: 'Sci-fi/Indie film ‧ 1h 30m',
                            up: 0,
                            down: 0,
                        },
                        {
                            id: 9,
                            title: 'The Man from Earth',
                            img: 'https://upload.wikimedia.org/wikipedia/en/3/3b/The_Man_from_Earth.png',
                            desc: 'Sci-fi/Indie film ‧ 1h 30m',
                            up: 0,
                            down: 0,
                        },
                        {
                            id: 10,
                            title: 'The Man from Earth',
                            img: 'https://upload.wikimedia.org/wikipedia/en/3/3b/The_Man_from_Earth.png',
                            desc: 'Sci-fi/Indie film ‧ 1h 30m',
                            up: 0,
                            down: 0,
                        },
                    ],
                    //top10 tvshows
                    tvshows: [
                        {
                            id: 1,
                            title: 'The Leftovers',
                            img: 'https://image.tmdb.org/t/p/w500/ri8xr223xBb2TeHX3GKypvQPV2B.jpg',
                            desc: 'Drama',
                            up: 0,
                            down: 0,
                        },
                        {
                            id: 2,
                            title: 'Better Call Saul',
                            img: 'https://cdn.shopify.com/s/files/1/0747/3829/products/mL2431.jpg?v=1571445543',
                            desc: 'Drama',
                            up: 0,
                            down: 0,
                        },
                        {
                            id: 3,
                            title: 'Breaking Bad',
                            img: 'https://fr.web.img5.acsta.net/pictures/19/06/18/12/11/3956503.jpg',
                            desc: 'Drama',
                            up: 0,
                            down: 0,
                        },
                        {
                            id: 4,
                            title: 'Game of Thrones',
                            img: 'https://hips.hearstapps.com/hmg-prod.s3.amazonaws.com/images/d7ng1slx4aewqjc-1558700218.jpg?crop=1xw:1xh;center,top&resize=480:*',
                            desc: 'Drama',
                            up: 0,
                            down: 0,
                        },
                        {
                            id: 5,
                            title: 'The Man from Earth',
                            img: 'https://upload.wikimedia.org/wikipedia/en/3/3b/The_Man_from_Earth.png',
                            desc: 'Sci-fi/Indie film ‧ 1h 30m',
                            up: 0,
                            down: 0,
                        },
                        {
                            id: 6,
                            title: 'The Man from Earth',
                            img: 'https://upload.wikimedia.org/wikipedia/en/3/3b/The_Man_from_Earth.png',
                            desc: 'Sci-fi/Indie film ‧ 1h 30m',
                            up: 0,
                            down: 0,
                        },
                        {
                            id: 7,
                            title: 'The Man from Earth',
                            img: 'https://upload.wikimedia.org/wikipedia/en/3/3b/The_Man_from_Earth.png',
                            desc: 'Sci-fi/Indie film ‧ 1h 30m',
                            up: 0,
                            down: 0,
                        },
                        {
                            id: 8,
                            title: 'The Man from Earth',
                            img: 'https://upload.wikimedia.org/wikipedia/en/3/3b/The_Man_from_Earth.png',
                            desc: 'Sci-fi/Indie film ‧ 1h 30m',
                            up: 0,
                            down: 0,
                        },
                        {
                            id: 9,
                            title: 'The Man from Earth',
                            img: 'https://upload.wikimedia.org/wikipedia/en/3/3b/The_Man_from_Earth.png',
                            desc: 'Sci-fi/Indie film ‧ 1h 30m',
                            up: 0,
                            down: 0,
                        },
                        {
                            id: 10,
                            title: 'The Man from Earth',
                            img: 'https://upload.wikimedia.org/wikipedia/en/3/3b/The_Man_from_Earth.png',
                            desc: 'Sci-fi/Indie film ‧ 1h 30m',
                            up: 0,
                            down: 0,
                        },
                    ],
                    //top10 anime
                    anime: [
                        {
                            id: 1,
                            title: 'Legend of the Galactic Heroes',
                            img: 'https://i.pinimg.com/originals/16/35/60/1635608ffe37658d4f85e7835e7acdd7.jpg',
                            desc: 'Novel series',
                            up: 0,
                            down: 0,
                        },
                        {
                            id: 2,
                            title: 'Cowboy Bebop',
                            img: 'https://cdn.vox-cdn.com/thumbor/KONOGbITLWDv-GzJXAk9GLMb9Zo=/0x0:1022x635/1400x1400/filters:focal(419x66:581x228):format(png)/cdn.vox-cdn.com/uploads/chorus_image/image/55114099/Screen_Shot_2017_06_06_at_10.50.19_AM.0.png',
                            desc: 'Animation',
                            up: 0,
                            down: 0,
                        },
                        {
                            id: 3,
                            title: 'Attack on Titan',
                            img: 'https://images-na.ssl-images-amazon.com/images/I/51oiT6FPaaL._AC_.jpg',
                            desc: 'Manga series',
                            up: 0,
                            down: 0,
                        },
                        {
                            id: 4,
                            title: 'Death Note',
                            img: 'https://cdn.europosters.eu/image/750/posters/death-note-from-the-shadows-i58005.jpg',
                            desc: 'Anime',
                            up: 0,
                            down: 0,
                        },
                        {
                            id: 5,
                            title: 'Parasyte',
                            img: 'https://images-na.ssl-images-amazon.com/images/I/81Ajzfd4wjL._AC_SL1500_.jpg',
                            desc: 'Manga series',
                            up: 0,
                            down: 0,
                        },
                        {
                            id: 6,
                            title: 'kaiji',
                            img: 'https://images-na.ssl-images-amazon.com/images/I/61VospzFQ0L._AC_.jpg',
                            desc: 'Manga series',
                            up: 0,
                            down: 0,
                        },
                        {
                            id: 7,
                            title: 'The Promised Neverland',
                            img: 'https://www.awesomepostersonline.com/uploads/2019-03-22/cbbe0910/00c656dd333.jpg',
                            desc: 'Manga series',
                            up: 0,
                            down: 0,
                        },
                        {
                            id: 8,
                            title: 'Vinland Saga',
                            img: 'https://ih1.redbubble.net/image.1057066243.8815/flat,750x,075,f-pad,750x1000,f8f8f8.jpg',
                            desc: 'Manga series',
                            up: 0,
                            down: 0,
                        },
                        {
                            id: 9,
                            title: 'Fullmetal Alchemist: Brotherhood',
                            img: 'https://images-na.ssl-images-amazon.com/images/I/91V6newzMNL._AC_SL1500_.jpg',
                            desc: 'Animation',
                            up: 0,
                            down: 0,
                        },
                        {
                            id: 10,
                            title: 'One Punch Man',
                            img: 'https://images-na.ssl-images-amazon.com/images/I/717aat3l-YL._AC_SL1224_.jpg',
                            desc: 'Manga series',
                            up: 0,
                            down: 0,
                        },
                    ],
                },
            }
        },
        mounted() {
            console.log('Component mounted.')
        },
    }
</script>

<style>
    #scroll::-webkit-scrollbar {
    width: 10px;               /* width of the entire scrollbar */
    }
    #scroll::-webkit-scrollbar-track {
    background: #edf2f7;        /* color of the tracking area */
    }
    #scroll::-webkit-scrollbar-thumb {
    border-radius: 50px;
    background-color: #676f7c;
    /* border: 3px solid orange;   */
    }
    #scroll {
    scrollbar-width: thin;          /* "auto" or "thin"  */
    scrollbar-color: #70798a #edf2f7;   /* scroll thumb & track */
    }
</style>
