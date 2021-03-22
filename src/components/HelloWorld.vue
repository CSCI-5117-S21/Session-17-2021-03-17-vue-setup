<template>
  <div class="hello">
    <span>{{count}}</span>
    <h1 v-if="count < 10">{{ msg+"!!!!" }}</h1>
    <button @click="count++"> click me </button>
    <input v-model="name" /> 
    <div :title="name+'!!!'" >happy </div>

    <editable-span @changed="name=$event"/>
  </div>
</template>

<script>
import editableSpan from './editableSpan.vue';
export default {
  components: { editableSpan },
  name: 'HelloWorld',
  props: {
    msg: String
  },
  data: function() {
    return {
      count: 0,
      name: "",
      names: ["daniel", "yang", "alexander", "ally", "alvin", "an"]
    };
  }
}
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
