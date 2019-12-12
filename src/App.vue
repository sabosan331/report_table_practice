<template>
      
      <div id="app">
      
      <div class="overall">
      <ul class="margin_zero">
        <li>目的</li>
        <li>参加者，発表者，残り企業</li>
        <li>内容</li>
        <li>感想</li>
        <li>今後</li>
      </ul>
      </div>
      
      <div class="items">
      <table>
        <tr class="coloms">
          <td>id</td>
          <td>タイトル</td>
          <td>発表者</td>
          <td>所属</td>
          <td>内容</td>
          <td>重要度</td>
        </tr>
        <tr v-for="(item, index) in items" v-bind:key="item.id" v-bind:style="styles[item.importance]">
          <td>{{index}}</td>
          <td>{{item.title}}</td>
          <td>{{item.auther}}</td>
          <td>{{item.belonging}}</td>
          <td>{{item.content}}</td>
          <td>{{item.importance}}</td>
        </tr>
      </table>

      </div>
     
    </div>


          
</template>

<script>
// import HelloWorld from './components/HelloWorld.vue'

export default {
  name: 'app',
  data: function() {
    return {
      items : [ 
        {
          title: "Machine Learning without data",
          auther: "sabosan",
          belonging: "sabo  Inc.",
          content: "There are no data with us, so I research about Machine Learning without data.",
          importance : 2,
        },
        {
          title: "",
          auther: "",
          belonging: "",
          content: "",
          importance : 3,
        }
      ],

      styles: [
        {
          backgroundColor: '#eeeeee',
          fontSize: '15px',
          color: '#222222'
        },
        { 
          backgroundColor: '#FAC031',
          fontSize: '15px',
          color: '#111111'
        },
        {
          backgroundColor: '#F27D2D',
          color: '#F2F2F2'
        },
        {
          backgroundColor: '#EC222E',
          color: '#F2F2F2'
        }
      ]
    }
  }
  // components: {
  //   HelloWorld
  // }
}
</script>

<style>
#app {
  font-family: 'Avenir', Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  height: 100vh;
  margin-top:0px;
  background-color : #222222;
  color : #eeeeee;
  overflow-y: auto;
}

body {
  margin:0px;
}


.coloms {
  background-color: #eeeeee;
  color:#0f0f0f;
}

.items{
  margin: 2% 5%;
  overflow-y: auto;

}

table {
  border-collapse: collapse;
  
}

table, th , td {
  border: solid 1px #aaaaaa;
}

th, td {
  padding: 5px 10px;
  text-align: left;
}

.overall{
  padding : 2% 3%;
}

.margin_zero{
  margin: 0px;
}

li {
  text-align : left;
}
</style>
