<template>
 
<div>
  <fieldset id="df">
  <legend>What's your degree</legend>
    <br>
  <input type="radio" id="hd" name="degree" value="hd" v-model="degree" />
  <label for="hd">High School Diploma</label><br />

  <input type="radio" id="ba" name="degree" value="ba" v-model="degree" />
  <label for="ba">Bachelor</label><br />
  </fieldset>
  <br>
<div v-show="degree == 'hd'">
    {{alert}}
  </div>
  <div v-show="degree == 'ba'">
    <select>
      <option disabled value="">Please select your university</option>
      <option value="c">Cambridge</option>
      <option value="m">MIT</option>
      <option value="o">Oxford </option>
  </select>
  </div>

</div>

</template>

<script>
export default {
  name: 'App',
  data() {
      return {
        
        degree:"",
        alert:'You are not allowed to fill out the form'
      }
    },
}
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  color: #2c3e50;
  margin-top: 60px;
}

#df{
  border: none;
}


</style>
