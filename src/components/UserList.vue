<template>
 
    <div>
        <div class="row">
            <input type="text" placeholder="Search" v-model="search">
        </div>
        <user-item v-for="(user, index) of searchTask" :key="user.name" :name="user.name" :img="user.img" :index="index"
        @selectItem="selectItem"></user-item>

    </div>
</template>
 
<script>
import UserItem from './UserItem.vue'
 
export default {
        data () {
        return {
            users:[
                {name:"Petya", img:"https://i.pinimg.com/originals/0c/a9/e2/0ca9e28dcb12dc698cfd2beda6d6fa64.jpg"},
                {name:"Vasya", img:"https://download-cs.net/steam/avatars/3412.jpg"},
                {name:"Kolya", img:"https://f1.upet.com/A_r2u6uZhnxA_x.jpg"}
            ],
            search:''
        }
  
    },
    components:{
        'user-item': UserItem
    },
    methods:{
        selectItem(index){
            this.$emit("selectItemUserList", this.users[index]);
        }
    },
    computed:{
        searchTask(){
            return this.users.filter(user => user.name.startsWith(this.search))
        }
    }
    
}
 
</script>