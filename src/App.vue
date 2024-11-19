<script>
import AsymptoteFinder from './components2/AsymptoteFinder.vue'
import CosineLaw from './components2/CosineLaw.vue'
import GregoryLeibnizPi from './components2/GregoryLeibnizPi.vue'

export default {
  components: {
    CosineLaw,
    AsymptoteFinder,
    GregoryLeibnizPi
  }
};
</script>

<template>
  
    <div>
    <CosineLaw />
    </div>
    <div>
    <AsymptoteFinder />
    </div>
    <div>
    <GregoryLeibnizPi />
    </div>
  
</template>


<style>
body {
    margin: 0;
    padding: 0;
    background-color: darkgrey;
    height: 700px;
}
h3 {
    text-align: center;
    font-size: 30px;
    font-weight: bold;
}
p {
    text-align: center;
    font-size: 18px;
    font-weight: bold;
    margin-bottom: 5px;
    margin-top: 10px;
}
input {
    margin-left: 60px;
    margin-right: 60px;
}
.result {
    background-color: rgb(111, 188, 111);
}
.calcbutton {
    background-color: green;
    width: 250px;
    height: 30px;
    margin-top: 20px;
    margin-left: 25px;
    margin-right: 25px;
    font-size: 18px;
    
}
</style>
