<template>
    <div>
        <li class="list-group-item">
            <div class="handle">
              <a href="javascript:;" @click="deletRider">删除</a>
            </div>
            <p class="user"><span >{{rider.name}}</span><span>说:</span></p>
            <p class="centence">{{rider.content}}</p>
          </li>
    </div>
</template>

<script>
    export default {
        props:['rider','deletAppR','index'],
        methods: {
          deletRider(){
            this.deletAppR(this.index)
          }
        },
    }
</script>

<style scoped>
  li {
  transition: .5s;
  overflow: hidden;
}

.handle {
  width: 40px;
  border: 1px solid #ccc;
  background: #fff;
  position: absolute;
  right: 10px;
  top: 1px;
  text-align: center;
}

.handle a {
  display: block;
  text-decoration: none;
}

.list-group-item .centence {
  padding: 0px 50px;
}

.user {
  font-size: 22px;
}
</style>