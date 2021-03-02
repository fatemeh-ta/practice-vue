<template>
  <div class="project-list">
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
    <div class="result">
      <!-- {{ showFilter }} -->
      <ul>
        <li v-for="item in showFilter" :key="item.index">
          {{ item }}
        </li>
      </ul>
    </div>
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
      developer : "sara"
    }
  },
  computed : {
    showFilter() {
      let result = this.projects.filter((arry) => arry.developer === this.developer && arry.yearstart > 1391 );
      let listproject = [];
      let i;
      // console.log(result);
      // console.log(result.length);
      for(i=0 ; i < result.length ; i++) {
        listproject[i]= result[i]["developer"] + " " + "get " + result[i]["projectname"] + " since " + result[i]["yearstart"] ;
        // console.log(listproject);
      }
      // console.log(listproject);
      return listproject
    }
  }
}
</script>

<style >
  .project-list {
    text-align: center;
  }
   .projects {
    margin: 0 auto;
    max-width: 100%;
  }
  .projects td,
  .projects th {
  border: 1px solid #ddd;
  padding: 8px 10px;
  }

  .projects tr:nth-child(even) {
    background-color: #f2f2f2;
  }

  .projects tr:hover {
    background-color: #ddd;
  }
  .result {
    margin: 16px;
  }
</style>

