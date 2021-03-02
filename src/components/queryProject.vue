<template>
  <div>
    <input type="text" v-model="search" placeholder="search...">
    <table class="projects">
      <tr v-for="(project , index) in projects" :key="index + project">
        <th> 
          {{ project.projectname }} 
        </th>
        <th>
          {{ project.developer }}
        </th>
        <th>
          {{ project.yearstart }}
        </th>
      </tr>
    </table>
    <div>
      <!-- {{ querysearch }} -->
    </div>
    <ul>
      <li v-for="item in querysearch" :key="item.index">
        {{ item }}
      </li>
    </ul>
  </div>
</template>

<script>
export default {
  data() {
    return {
      projects : [
        { projectname : "eghtesadnews",
          developer : "sara",
          yearstart : 1390
        },
        { projectname : "55online",
          developer : "sara",
          yearstart : 1390
        },
        { projectname : "shayanews",
          developer : "ehsan",
          yearstart : 1391
        },
        { projectname : "kargah",
          developer : "ehsan",
          yearstart : 1391
        },
        { projectname : "rasadeghtesadi",
          developer : "sara",
          yearstart : 1392
        },
      ],
      search : ""
    }
  },
  computed : {
    querysearch() {
      let result;
      let listproject = [];
      result =this.projects.filter(arry => arry.developer === this.search);
      for(let i=0 ; i<result.length ; i++) {
        listproject[i] = result[i]["developer"] + " " + "has " + result[i]["projectname"] + " " ;
      }
      return listproject
    }
  }
}
</script>

<style  scoped>

</style>