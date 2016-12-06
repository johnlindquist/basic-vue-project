<template>
  <div>
    <ul>
      <li v-for="person in people">{{person.name}}</li>
    </ul>
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
