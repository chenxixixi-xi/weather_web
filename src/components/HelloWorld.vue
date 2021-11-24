<template>
  <div class="hello">
    <el-radio-group v-model="adress" size="small"> </el-radio-group>
    <div style="margin: 20px"></div>
    <el-form
      :label-position="labelPosition"
      label-width="80px"
      :model="location"
    >
      <el-form-item label="location ">
        <el-input v-model="location.name"></el-input>
      </el-form-item>
    </el-form>

    <el-button type="primary" @click="show()">get location</el-button>

    <el-radio-group v-model="labelPosition" size="small"> </el-radio-group>
    <div style="margin: 20px"></div>
    <el-form
      :label-position="labelPosition"
      label-width="80px"
      :model="formLabelAlign"
    >
      <el-form-item label="longitude ">
        <el-input v-model="formLabelAlign.name"></el-input>
      </el-form-item>
      <el-form-item label="latitude ">
        <el-input v-model="formLabelAlign.region"></el-input>
      </el-form-item>
    </el-form>

    <el-button type="primary" @click="showWeather()">get Data</el-button>
  </div>
</template>

<script>
import axios from 'axios'
export default {
  data() {
    return {
      labelPosition: "left",
      formLabelAlign: {
        name: "",
        region: "",
        type: "",
      },
      adress: "left",
      location: {
        name: "",
        type: "",
      },
    };
  },
  methods: {
    show() {
      console.log(this.location.name);

      window.open(`https://api.caiyunapp.com/v2/place?token=VKC3aGqblsPQTRQT&lang=en_US&query=${this.location.name}`,'_blank'); 

      
    },
     showWeather() {
      console.log(this.formLabelAlign.name);

      window.open(`https://api.caiyunapp.com/v2.5/VKC3aGqblsPQTRQT/${this.formLabelAlign.name},${this.formLabelAlign.region}/realtime.json?lang=en_US`,'_blank'); 
    
    },
  },
};
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
