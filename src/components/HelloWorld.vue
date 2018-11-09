<template>
  <div class="hello">
    <h1>{{ msg }}</h1>
    <ul>
      <li v-for="elem in commentary">
        "{{elem.comment}}" - {{elem.by}}
      </li>
    </ul>
    <div id="tilefish_appreciation">
      Show your support for the tilefish by SMASHING this button!!!!<br>
      <button class="btn btn-primary" v-on:click="counter++">Click to donate $5 to the WTF (World Wide Tilefish Foundation &copy;)</button><br>
      Money Donated: ${{counter*5}}
    </div>
  </div>
</template>

<script>
export default {
  name: 'HelloWorld',
  data () {
    return {
      commentary: [
        {comment: 'This fish is rad', by: 'Max Weber'},
        {comment: 'I wish more people knew about this amazing fish', by: 'Barack Obama'},
        {comment: 'I did not know that these fish could <FUN_FACT>!', by: 'Johnny Cash'},
        {comment: 'Tilefish are cooler than Guppies!!!!', by: 'Munis Thahir'}
      ],
      counter: 0,
      msg: 'The Tilefish.'
    }
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
h1, h2 {
  font-weight: normal;
}
ul {
  list-style-type: none;
  padding: 0;
}
li {
  width: 100vw;
  display: inline-block;
  margin: 0 10px;
}
a {
  color: #42b983;
}
</style>
