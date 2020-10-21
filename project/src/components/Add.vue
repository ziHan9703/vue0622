<template>
  <div>
    <div class="col-md-4">
      <form class="form-horizontal">
        <div class="form-group">
          <label>用户名</label>
          <input
            type="text"
            class="form-control"
            placeholder="用户名"
            v-model="name"
          />
        </div>
        <div class="form-group">
          <label>评论内容</label>
          <textarea
            class="form-control"
            rows="6"
            placeholder="评论内容"
            v-model="content"
          ></textarea>
        </div>
        <div class="form-group">
          <div class="col-sm-offset-2 col-sm-10">
            <button
              type="button"
              class="btn btn-default pull-right"
              @click="addRider"
            >
              提交
            </button>
          </div>
        </div>
      </form>
    </div>
  </div>
</template>

<script>
export default {
  props: ["riders", "addAppR"],
  data() {
    return {
      name: "",
      content: "",
    };
  },
  methods: {
    addRider() {
      let { name, content } = this;
      if (name.trim() && content.trim()) {
        let id = Date.now();
        let obj = {
          id,
          name,
          content,
        };
        this.addAppR(obj);
      }
      this.name = "";
      this.content = "";
    },
  },
};
</script>

<style scoped>
</style>