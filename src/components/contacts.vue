<template>
  <div class="contacts">
     <p>Contacts</p>
        <ul>
            <li>mail:{{ mail }}</li>
            <li>skype: tim.bikbaev </li>
            <li>phone: +380671014882</li>
            <li>telegram: @t_bikbaev</li>
        </ul>
  </div>
</template>

<script>
export default {
  name: 'contacts',
  props: {
    mail: String
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
