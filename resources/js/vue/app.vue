<template>
    <div class="todo-list-container">
        <div class="heading">
            <h2 id="title">Todo List</h2>
            <create-item
                v-on:reloadlist="getListItems()" 
            />
        </div>
        <list-view 
            :items="items"
            v-on:reloadlist="getListItems()" />
    </div>
</template>
<script>
import createItem from './createItem.vue'
import listView from './listView.vue'

export default {
    components:{
        createItem,
        listView
    },
    data: function() {
        return {
            items: []
        }
    },
    methods: {
        getListItems(){
            axios.get('/api/items')
            .then(response => {
                this.items = response.data
            })
            .catch(error => {
                console.log(error)
            })
        }
    },
    created(){
        this.getListItems()
    }
}
</script>
<style scoped>
.todo-list-container{
    width: 350px;
    margin: auto;
}
.heading{
    background: #e6e6e6;
    padding: 10px;
}
#title{
    text-align: center;
}
</style>