<template>
  <div class="hello">
    <h1>{{ msg }}</h1>
    
    <h2>Link to my practices</h2>
    <ul>
      <li><a href="https://github.com/TheCrow95T">Github</a></li>
      <li><a href="https://replit.com/@TheCrow95T">Replit</a></li>
      <li><a href="https://www.codewars.com/users/thecrow95_">Codewars</a></li>
    </ul>

    <h2>Some random picture taken by me</h2>
    <div class="img-div">
      <img src="../assets/image1.jpg" alt="">
      <img src="../assets/image2.jpg" alt="">
      <img src="../assets/image3.jpg" alt="">
      <img src="../assets/image4.jpg" alt="">
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
h2 {
  font-size: 24px;
  margin-top: 40px;
  margin-bottom: 15px;
  font-weight: bold;
}

ul {
  list-style-type: none;
  padding: 0;
}

li {
  display: inline-block;
  border-radius: 25px;
  font-weight: bold;
  background-color: rgb(163, 184, 201);
  margin: 10px 10px;
  padding: 15px 30px;
}

a {
  color: #6554b1;
}

.img-div {
  display: flex;
  justify-content: center;
  flex-wrap: wrap;
}

img {
  max-width: 40%;
  margin: 20px 20px;
}

@media (max-width: 700px) {
  img {
    max-width: 100%;
  }
}
</style>
