<template>
    <div>
          <Header></Header>
    <div class="container">
      <Add :riders="riders" :addAppR="addAppR"></Add>
        <List :riders="riders" :deletAppR="deletAppR"></List>
    </div>
    </div>
</template>

<script>
import Header from '@/components/Header';
import Add from '@/components/Add';
import List from '@/components/List';
    export default {
        components:{
            Header,
            Add,
            List
        },
        data() {
            return {
                riders:[
                    {id:1,name:'甲斗',content:'逼王'},
                    {id:2,name:'时王',content:'平成最强'},
                    {id:3,name:'空我',content:'平成第一人'}
                ]
            }
        },
        methods: {
            addAppR(obj){
                this.riders.unshift(obj)
            },
            deletAppR(index){
                this.riders.splice(index,1);
            }
        },
    }
</script>

<style scoped>

</style>