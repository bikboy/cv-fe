<template>
  <div id="skills" >
     <h2>Skills</h2>
      <div id="clouds">
        <h4>Clouds</h4>
        <div v-for="skill in skills.skills" :key="skill">
          <template v-if="skill.category == 'clouds'">
            {{skill.name}}
          </template>
        </div>
      </div>
      <div id="kubernetes">
        <h4>Kubernetes</h4>
        <div v-for="skill in skills.skills" :key="skill">
          <template v-if="skill.category == 'kubernetes'">
            {{skill.name}}
          </template>
        </div>
      </div>
      <div id="iaac">
        <h4>IaaC</h4>
        <div v-for="skill in skills.skills" :key="skill">
          <template v-if="skill.category == 'iaac'">
            {{skill.name}}
          </template>
        </div>
      </div>
      <div id="ci">
        <h4>CI</h4>
        <div v-for="skill in skills.skills" :key="skill">
          <template v-if="skill.category == 'ci'">
            {{skill.name}}
          </template>
        </div>
      </div>
      <div id="scripting">
        <h4>Scripting</h4>
        <div v-for="skill in skills.skills" :key="skill">
          <template v-if="skill.category == 'scripting'">
            {{skill.name}}
          </template>
        </div>
      </div>
      <div id="db">
        <h4>DB</h4>
        <div v-for="skill in skills.skills" :key="skill">
          <template v-if="skill.category == 'db'">
            {{skill.name}}
          </template>
        </div>
      </div>
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
    fetch("http://localhost:8080/api/skills")
      .then(response => response.json())
      .then(data => (this.skills = data));
  },
  render(h) {
    return h("div", "TEST")
  }
  // computed: {
    
  //   clouds: function () {
  //     return this.skills.filter(i => i.skills.category === 'clouds')
  //   },
  //   kubernetes: function () {
  //     return this.skills.filter(i => i.skills.category === 'kubernetes')
  //   }
  // }
}

</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
#skills {
	display: flex;
	margin: 20px;	
}
#clouds{
	margin: 20px;
}
#kubernetes {
	margin: 20px;
}
#iaac{
	margin: 20px;
}
#ci {
	margin: 20px;
}
#scripting{
	margin: 20px;
}
#db {
	margin: 20px;
}
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
