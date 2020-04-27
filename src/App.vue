<template>
  <div class="container" id="app">
    <div class="row">
      <div class="col s4">
        <tag-users-list @selectItemUserList="changeName"></tag-users-list>
      </div>

      <div class="col s8">
        <tag-main :selectName="selectName"></tag-main>
      </div>
    </div>
  </div>
</template>

<script>
import UsersList from './components/UserList.vue';
import MainComponent from './components/Main.vue';

export default {
  name: 'app',
  data () {
    return {
      selectName:''
    }
  },
  components:{
    'tag-users-list' : UsersList,
    'tag-main': MainComponent
  },
  methods:{
    changeName(user){
      this.selectName=user;
    }
  }
  
}
</script>

<style>

</style>
