<template>
 
    <div>
       
        <div class="card blue-grey darken-1">
            <div class="chip">
            <img :src="img" alt="Contact Person">
            {{name}}
            </div>
            <a @click="selectItemClicked(index)" class="waves-effect waves-light btn">button</a>
            
        </div>
    </div>
</template>

<script>

 
export default {
        data () {
        return {
           
        }
  
    },
    props: ['name', 'img', 'index'],
    methods:{
        selectItemClicked(index){
            this.$emit("selectItem", index);
        }
    }
}
 
</script>