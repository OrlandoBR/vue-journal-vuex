<template>
  <div class="entry-list-container">
    <div class="px-2 pt-2 mb-2">
      <input type="text" class="form-control" placeholder="Buscar entrada" />
    </div>
    <div class="entry-scrollarea">
        <EntryV v-for="item in 100" :key="item"/>
    </div>
  </div>
</template>

<script>
import { defineAsyncComponent } from 'vue';
export default {

    components:{
        EntryV: defineAsyncComponent(()=> import('./EntryV.vue'))
    }

};
</script>

<style scoped>
.entry-list-container{
border-right: 1px solid #2c3e50;


}
.entry-scrollarea{
height: calc(100vh - 120px);
overflow-y: scroll;
}
</style>