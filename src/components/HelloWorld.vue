<template>
  <div class="hello">
    <h1>{{ msg }}</h1>
    <p>
      Jacks is a naturally amazing software developer 
      and designer and if you want to see 
      more of their work check out 
      <a href="https://j4cks.com" target="_blank" rel="noopener">j4cks.com</a>.
    </p>
    <h3>~Time is a human phenomenon~</h3>
    <ul>
      <li><a href="https://jacks.media" target="_blank" rel="noopener">jacks.media</a></li>
      <li>2021</li>
    </ul>
  </div>
</template>

<script>
export default {
  name: 'HelloWorld',
  props: {
    msg: String
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
h1 {
  font-size: 4.4vw;
}
h3 {
  margin: 40px 0 0;
  font-size: 3.6vw;
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
  color: navy;
}
p {
  text-align: center;
  font-size: 3.2vw;
}
</style>
