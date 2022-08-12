<template>
<div>
    {{title}}
     <button @click=changetitle()>Change</button>
     <h2>Al blog posts</h2>
     <input type="text" v-model="searchTerm">
     <hr>
     <!-- <div v-for="post in posts" >
        <h6>{{post.title}}</h6>

     </div> -->
     <div v-for="post in filtersearch" :key="post.id">
        <h6>{{post.title}}</h6>
        <p>{{post.body | program}}</p>
     
     </div>
</div>

</template>

<script>
import axios from 'axios'
export default{
    name:'Hook',
    data(){
        return{
            title:"Hook main data",
            posts:[],
            searchTerm: ''
        }
    },
    computed:{
        filtersearch(){
            return this.posts.filter(post=>{
                return post.title.match(this.searchTerm)
            })
        }

    },
    methods:{
        changetitle(){
            this.title="changeable hook data"
        }

    },
    beforeCreate(){
        alert('this is before hook')
    },
    created(){
        axios.get('https://jsonplaceholder.typicode.com/posts')
        .then(response=>{
            // console.log(response)
            this.posts=response.data
        })
        .catch

    },
}

</script>

<style>

</style>