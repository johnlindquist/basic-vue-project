<template>
    <div>
        <h1>{{person.name}}</h1>
        
    </div>
</template>
<script>
import axios from 'axios'

const api = `https://swapi-json-server-nvaxelgbew.now.sh/people`

export default {
  data({params}){return axios.get(api + `/${params.id}`)
    .then(res => ({person:res.data}))
  }
}
</script>