<template>
  <div class="contacts">
     <p>Contacts</p>
        {{ contacts }}
        <!-- <ul>
            <li>mail:{{ mail }}</li>
            <li>skype: tim.bikbaev </li>
            <li>phone: +380671014882</li>
            <li>telegram: @t_bikbaev</li>
        </ul> -->
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
    fetch("http://localhost:5000/api/contacts")
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
