<template>
  <div>
      <div v-for="person in people">
        <router-link :to="'/user/' + person.id">{{person.name}}</router-link>
      </div>   
  </div>
</template>
<script>
import axios from 'axios'

const api = `https://swapi-json-server-nvaxelgbew.now.sh/people`

export default {
  data(){return axios.get(api)
    .then(res => ({people:res.data}))
  }
}
</script>
