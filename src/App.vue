<template>
  <div id="app">
    <div class="computed"> calculator with Computed </div>
    <Calculator></Calculator>
    <div class="method"> calculator with Method </div>
    <CalculatorMethod></CalculatorMethod>
    <div class="method"> show filter array </div>
    <Projects></Projects>
    <div class="method"> show filter array with Computed </div>
    <ProjectsCompute></ProjectsCompute>
    <div class="method"> show filter array with Computed </div>
    <QueryProject></QueryProject>
  </div>
</template>

<script>
import Calculator from './components/calculator';
import CalculatorMethod from './components/calculatorMethod';
import Projects from './components/projects';
import ProjectsCompute from './components/projectsCompute';
import QueryProject from './components/queryProject';
export default {
  name: 'App',
  data() {
    return {

    }
  },
  components : {
    Calculator,
    CalculatorMethod,
    Projects,
    ProjectsCompute,
    QueryProject
  }
 
}
</script>

<style>
#app {
  text-align: center;
}
.computed,
.method {
  text-align: center;
  margin: 24px 0;
  color: rgb(129, 6, 6);
}
</style>
