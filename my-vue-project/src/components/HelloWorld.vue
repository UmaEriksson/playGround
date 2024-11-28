

<template>
  <div class = "wrapper">
  <div class = "picture">
    <img class ="pic" src="..\assets\pic.png">
  </div>
  <div class="hello">
   <h1>Let's give this a try</h1>
  </div>

  <div class ="content">
    
  </div>
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
:global(body){

  background-color:#ebedda;
}
.wrapper{
  display: flex;
  flex-direction: row;
  height: 100%;
  width: 100%;
  
}
.picture{
  border-radius: 50%;

}
.pic{

 width: 20vw;
 height: 20vw;
 position: fixed;
 border-radius: 50%;
 overflow: hidden;
 object-fit: cover;
 border-style: solid;
 border-width: 5px;
 border-color: #87BAAB;
 top: 1%;
 
}

.hello{
  text-align: center;
  overflow: hidden; /* Ensures the content is not revealed until the animation */
  border-right: .15em solid #87BAAB; /* The typwriter cursor */
  white-space: nowrap; /* Keeps the content on a single line */
  margin: auto; /* Gives that scrolling effect as the typing happens */
  letter-spacing: .15em; /* Adjust as needed */
  animation: 
    typing 3.5s steps(40, end),
    blink-caret .75s step-end infinite;
}

/* The typing effect */
@keyframes typing {
  from { width: 0 }
  to { width: 100% }
}

/* The typewriter cursor effect */
@keyframes blink-caret {
  from, to { border-color: transparent }
  50% { border-color: #87BAAB; }
}
h1 {
 
 font-family: "Lucida Console", "Courier New", monospace;
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
  color: #87BAAB;
}
</style>
