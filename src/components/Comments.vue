<template>
    
    <div>
        <div class="row">
            <textarea v-model="newComm" placeholder="Коментар" class="col s10"></textarea>
            <button @click="addComm" class="btn waves-effect waves-light col s2" type="submit" name="action">send
            </button>
        </div>
        <tag-comm-item v-for="(item, index) in comments" :key="index" :item="item"></tag-comm-item>
    </div>

</template>



<script>
import CommentsItem from './CommentsItem';
 
export default {
        data () {
        return {
            comments:[
                {img:"https://i.pinimg.com/originals/0c/a9/e2/0ca9e28dcb12dc698cfd2beda6d6fa64.jpg", name:"Petya", text:"Lorem, ipsum dolor sit amet consectetur adipisicing elit. est optio error eos soluta."},
                {img:"https://download-cs.net/steam/avatars/3412.jpg", name:"Vasya", text:"hi"}
            ],
            newComm:''
        }
        
  
    },
    components:{
    'tag-comm-item': CommentsItem
    },
    methods:{
        addComm(){
            if(this.newComm != '' && this.selectUser != ''){
                this.comments.push({img: this.selectUser.img, name: this.selectUser.name, text: this.newComm});
                this.newComm='';
            }
        }
    },
    props:['selectUser']
    
}
 
</script>