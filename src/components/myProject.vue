<template>
  <div class="project-section">
    <h3>Projects</h3>
    <div class="static" v-bind:key="item.id" v-for="item in projects" v-bind:class="{ 'card-left': item.isLeft, 'card-right': item.isRight }">
        <a v-bind:href="item.url" target="_blank"><img v-bind:src="item.bgUrl" width="500" height="200">
        <h4>{{item.title}}</h4></a>

    </div>
  </div>
</template>

<script>
export default {
  name: "myProject",
  props: ["projects"]
};
</script>

<style scoped>
a {
    text-decoration: none;
    color: white;
}
.project-section {
  color: white;
  font-size: 150%;
  text-align: center;
  padding-top: 150px;
  font-family: "Roboto", sans-serif;
}
.card-left {
    color: white;
    border: 1px solid white;
    width: 500px;
    margin-left: 100px;
    margin-top: 100px;
    float: left;
    box-shadow: 5px 10px 5px;
}


.card-right {
    color: white;
    border: 1px solid white;
    width: 500px;
    margin-right: 100px;
    margin-top: 100px;
    float: right;
    box-shadow: 5px 10px 5px;
}

@media (min-width: 768px) and (max-width: 979px) {
  * {
    color: #f00;
  }
}
</style>