<template>
    
    <div class="card-panel blue lighten-5">
        <div class="chip">
            <img :src="item.img" alt="Contact Person">
            {{item.name}}
        </div>
        <p>{{item.text}}</p>
    </div>

</template>



<script>

 
export default {
        data () {
        return {
           
        }
  
    },
    props:['item']
    
}
 
</script>