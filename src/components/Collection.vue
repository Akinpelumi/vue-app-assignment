<template>
    <div>
        <input type="text" placeholder="Search" />
        <div class="image__wrapper" v-show="duration">
            <div class="images" v-for="(item, index) in myCollection" :key="index">
                <h2>{{item.Name}}</h2>
                <h4><i>{{item.Type}}</i></h4>
                <img :src="item.Url" class="img"/>
                <br/>
                <button class="button" @click="deleted(index)">Delete</button>
            </div>
        </div>
    </div>
</template>

<script>
    export default{
        name: 'Collection',
        data() {
            return {
                myCollection: [
                    {
                        Name: "John Frusciante",
                        Type: "music",
                        Url: "http://static.tvmaze.com/uploads/images/original_untouched/60/151357.jpg"
                    },
                    {
                        Name: "Reservoir Dogs",
                        Type: "movie",
                        Url: "http://static.tvmaze.com/uploads/images/original_untouched/60/151357.jpg"
                    },
                    {
                        Name: "Foo Fighters",
                        Type: "music",
                        Url: "http://static.tvmaze.com/uploads/images/original_untouched/60/151357.jpg"
                    },
                    {
                        Name: "Pearl Jam",
                        Type: "music",
                        Url: "http://static.tvmaze.com/uploads/images/original_untouched/60/151357.jpg"
                    },
                    {
                        Name: "Sublime",
                        Type: "music",
                        Url: "http://static.tvmaze.com/uploads/images/original_untouched/60/151357.jpg"
                    },
                    {
                        Name: "Inglourious Basterds",
                        Type: "movie",
                        Url: "http://static.tvmaze.com/uploads/images/original_untouched/60/151357.jpg"
                    },
                    {
                        Name: "Incubus",
                        Type: "music",
                        Url: "http://static.tvmaze.com/uploads/images/original_untouched/60/151357.jpg"
                    },
                    {
                        Name: "Audioslave",
                        Type: "music",
                        Url: "http://static.tvmaze.com/uploads/images/original_untouched/60/151357.jpg"
                    },
                    {
                        Name: "Jackie Brown",
                        Type: "movie",
                        Url: "http://static.tvmaze.com/uploads/images/original_untouched/60/151357.jpg"
                    },
                    {
                        Name: "Nirvana",
                        Type: "music",
                        Url: "http://static.tvmaze.com/uploads/images/original_untouched/60/151357.jpg"
                    },
                    {
                        Name: "The Big Lebowski",
                        Type: "movie",
                        Url: "http://static.tvmaze.com/uploads/images/original_untouched/60/151357.jpg"
                    },
                    {
                        Name: "Goodfellas",
                        Type: "movie",
                        Url: "http://static.tvmaze.com/uploads/images/original_untouched/60/151357.jpg"
                    },
                    {
                        Name: "Guns N' Roses",
                        Type: "music",
                        Url: "http://static.tvmaze.com/uploads/images/original_untouched/60/151357.jpg"
                    },
                    {
                        Name: "Death Proof",
                        Type: "movie",
                        Url: "http://static.tvmaze.com/uploads/images/original_untouched/60/151357.jpg"
                    },
                    {
                        Name: "The Offspring",
                        Type: "music",
                        Url: "http://static.tvmaze.com/uploads/images/original_untouched/60/151357.jpg"
                    },
                    {
                        Name: "Django Unchained",
                        Type: "movie",
                        Url: "http://static.tvmaze.com/uploads/images/original_untouched/60/151357.jpg"
                    },
                    {
                        Name: "Rage Against The Machine",
                        Type: "music",
                        Url: "http://static.tvmaze.com/uploads/images/original_untouched/60/151357.jpg"
                    },
                    {
                        Name: "Snatch",
                        Type: "movie",
                        Url: "http://static.tvmaze.com/uploads/images/original_untouched/60/151357.jpg"
                    },
                    {
                        Name: "Trainspotting",
                        Type: "movie",
                        Url: "http://static.tvmaze.com/uploads/images/original_untouched/60/151357.jpg"
                    },
                    {
                        Name: "Weezer",
                        Type: "music",
                        Url: "http://static.tvmaze.com/uploads/images/original_untouched/60/151357.jpg"
                    }
                ]
            }
        },
        methods: {
            deleted(index) {
            this.myCollection.splice(index, 1)
            },
            duration: function(){
                let v = this;
                setTimeout(function(){
                    v.item.Name;
                    v.item.Type;
                    v.item.Url;
                }, 5000)
            }
        },
        mounted() {
            this.duration()
        } 
    }
</script>
<style scoped>
.image__wrapper {
    margin-top: 50px;
    display: grid;
    grid-template-columns: auto auto auto;
}
.img {
    height: 400px;
    width: 400px;
}
.button {
    margin-bottom: 20px;
    width: 96%;
    background: lightseagreen;
    color: white;
    height: 30px;
}
input{
    width: 50%;
    background: lightskyblue;
    color: white;
    border-style: none;
    height: 40px;
    border: 2px solid black;
    border-radius: 30px;
    padding-left: 20px;
}
</style>
