<template>
  <div class="contacts">
     <p>Contacts</p>
        <!-- {{ contacts }} -->
        <ul class="flex-container row-reverse">
          <li class="flex-item" v-for="(value, type) in contacts" :key="type">{{type}} : {{value}}</li>
        </ul>
  </div>
</template>

<script>
export default {
  name: 'contacts',
  data() {
    return {
      contacts: null
    };
  },
  created() {
    // Simple GET request using fetch
    fetch("http://localhost:8080/api/contacts")
      .then(response => response.json())
      .then(data => (this.contacts = data));
  }
}

</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
h3 {
  margin: 40px 0 0;
}
/* ul {
  list-style-type: none;
  padding: 0;
}
li {
  display: inline-block;
  margin: 0 10px;
} */
a {
  color: #42b983;
}
</style>
