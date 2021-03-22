<template>
  <div class="hello">
    <span>{{count}}</span>
    <h1 v-if="count < 10">{{ msg+"!!!!" }}</h1>
    <button @click="count++"> click me </button>
    <div :title="name+'!!!'" >happy </div>
<br/>
    <editable-input v-model="name"/> value:{{name}}
<br/>
    <keyword word="apple">A <b>DELICOUS</b> TREAT</keyword>
<br/>
    <rating-interface v-model="star" :prediction="4"/>
  </div>
</template>

<script>
import EditableInput from './editableInput.vue';
import Keyword from './keyword.vue';
import RatingInterface from './ratingInterface.vue';
export default {
  components: { EditableInput, Keyword, RatingInterface },
  name: 'HelloWorld',
  props: {
    msg: String
  },
  data: function() {
    return {
      count: 0,
      star: -1,
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
