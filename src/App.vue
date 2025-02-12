<template>
  <div>
    <raspberry-list :raspberries="raspberries"/>

  </div>
</template>

<script>
import { raspberryList } from './constants/raspberries';
import RaspberryList from './components/RaspberryList';
export default {
  name: 'App',
  components: { RaspberryList },
  data() {
    return {
      raspberries: raspberryList,
    }
  },
    
  }
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #fff;
  background-color: #000;
  margin-top: 60px;
}
</style>