<template>
  <div class="skills">
     <h1>Skills</h1>
        <p v-for="skill in skills" :key="skill">{{skill}}</p>
        <ul class="flex-container row-reverse">
          <li class="flex-item" v-for="type in skills.clouds" :key="type">{{type}}</li>
        </ul>
  </div>
</template>

<script>
export default {
  name: 'skills',
  data() {
    return {
      skills: null
    };
  },
  created() {
    // Simple GET request using fetch
    fetch("http://localhost:8080/api/skills")
      .then(response => response.json())
      .then(data => (this.skills = data));
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
