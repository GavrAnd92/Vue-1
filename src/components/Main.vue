<template>
    
    <div>
        <h3>Набирає текст: {{selectName.name}}</h3>
        <tag-comm :selectUser="selectName"></tag-comm>
    </div>

</template>



<script>
import Comments from './Comments';

 
export default {
        data () {
        return {
 
        }
  
    },
    props:['selectName'],
    components:{
    'tag-comm': Comments
    }
}
 
</script>