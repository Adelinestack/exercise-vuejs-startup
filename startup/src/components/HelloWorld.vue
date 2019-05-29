<template>
  <div class="hello">
    <h2>{{ texte }}</h2>
    <p>
      <a :href="url" target="_blank" rel="noopener">{{texte}}</a>
    </p>
    <h3>{{name}}</h3>
    <p>Counter : {{counter}}</p>
    <p>isVisible : {{isVisible}}</p>
    <ul>
      <li v-for="({name, isMaster}, id) in team" :key="id">
        <span v-if="isMaster">{{name}}</span>
      </li>
    </ul>
    <input type="text" v-model="name">
  </div>
</template>


<script>
export default {
  name: "HelloWorld",
  data: () => ({
    name: "Stackerine",
    counter: 0,
    isVisible: false,
    team: [
      { name: "Adeline", isMaster: true },
      { name: "Pauline", isMaster: true },
      { name: "Axelle", isMaster: true },
      { name: "Joe", isMaster: false }
    ]
  }),
  props: {
    url: String,
    texte: String,
    bool: Boolean
  }
};
</script>


<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
h3 {
  margin: 40px 0 0;
}
ul {
  list-style-type: none;
  padding: 0;
}
li {
  display: inline-block;
  margin: 0 10px;
}
a {
  color: #42b983;
}
</style>
