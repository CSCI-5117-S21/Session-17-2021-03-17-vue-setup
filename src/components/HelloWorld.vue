<template>
  <div class="hello">
    <span>{{count}}</span>
    <h1 v-if="count < 10">{{ msg+"!!!!" }}</h1>
    <button @click="count++"> click me </button>
    <input v-model="name" /> 
    <div :title="name+'!!!'" >happy </div>

    <editable-input v-model="name"/>
  </div>
</template>

<script>
import EditableInput from './editableInput.vue';
export default {
  components: { EditableInput },
  name: 'HelloWorld',
  props: {
    msg: String
  },
  data: function() {
    return {
      count: 0,
      name: "test",
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
