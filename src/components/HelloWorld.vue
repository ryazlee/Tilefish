<template>
  <div class="hello">
    <span id="header">
      <img id="seaweed_image" class="animated infinite jello" :src="seaweed_img"/>
      <img id="tilefish_image" class="animated infinite pulse" :src="tilefish_img"/>
      <img id="seaweed_image" class="animated infinite jello" :src="seaweed_img"/>
    </span>
    <h1>{{ msg }}</h1>
    <iframe width="500" height="400" src="https://www.youtube.com/embed/BnuBvBB1v_k" frameborder="0" allow="accelerometer; autoplay; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe>
    <div id="tilefish_commentary">
      <ul>
        <li v-for="elem in commentary" :key="elem.comment">
          <i>"{{elem.comment}}" - {{elem.by}}</i>
        </li>
      </ul>
    </div>
    <div id="tilefish_appreciation">
      Show your support for the tilefish by SMASHING this button!!!!<br>
      <button class="btn btn-primary" v-on:click="counter++">Click to donate $5 to the WTF (Worldwide Tilefish Foundation &copy;)</button><br>
      Money Donated: ${{counter*5}}
    </div>
    <div id="tilefish_funfacts">
      Need reasons to donate?  Check out these fun facts!<br>
      <ol>
        <li v-for="elem in fun_facts" :key="elem">
          {{elem}}
        </li>
      </ol>
    </div>
    <div id="tilefish_sources">
      <ul>
        <li v-for="elem in sources" :key="elem">
          <a v-bind:href="elem">{{ elem }}</a>
        </li>
      </ul>
    </div>
    <div id="watermark">Created by Ryan Lee for IBC82 (Fall 2018)</div>
  </div>
</template>

<script>
export default {
  name: 'HelloWorld',
  data () {
    return {
      tilefish_img: require('../assets/tilefish.png'),
      seaweed_img: require('../assets/seaweed.png'),
      commentary: [
        {comment: 'This fish is rad', by: 'Max Weber'},
        {comment: 'I wish more people knew about this amazing fish', by: 'Barack Obama'},
        {comment: 'I did not know that these fish could <FUN_FACT>!', by: 'Johnny Cash'},
        {comment: 'Tilefish are cooler than Guppies!!!!', by: 'Munis Thahir'}
      ],
      fun_facts: [
        'These fish can live up to 50 years',
        'A tilefish diet consists of eels, worms, crabs, sea cucumbers, shrimps, and clams',
        'Tilefish sexually mature at age 6',
        'If you are pregnant, it is not a good idea to consume this fish',
        'Tilefish lay 2 - 8 billion eggs during spawning'
      ],
      sources: [
        'http://www.animalspot.net/tilefish.html',
        'https://www.encyclopedia.com/plants-and-animals/animals/vertebrate-zoology/tilefish'
      ],
      counter: 0,
      msg: 'The Tilefish.'
    }
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style>
#tilefish_commentary {
  display: block;
  margin-left: -45px;
}
#tilefish_commentary ul {
  list-style-type: none;
}
#tilefish_commentary li {
  display: block;
}
a {
  color: #42b983;
}
#tilefish_funfacts {
  max-width: 600px;
  display: block;
  font-size: 150%;
  text-align: center;
  margin: auto;
  margin-top: 25px;
}
#tilefish_funfacts ol {
  max-width: 85%;
  text-align: left;
  margin: auto;
}
#tilefish_funfacts li {
  font-size: 70%;
}
#tilefish_sources {
  display: block;
  margin-left: -45px;
  font-size: 35%;
}
#tilefish_sources ul {
  list-style-type: none;
}
#tilefish_sources li {
  display: block;
}
#header #seaweed_image{
  width: 10vw;
}
#header #tilefish_image{
  width: 50vw;
}
h1 {
  font-size: 300%;
}
#watermark {
  padding: 10px;
}
</style>
