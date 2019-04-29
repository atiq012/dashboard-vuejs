<template>
  <div id="app">
    <el-container>
      <el-aside width="230px">
        <div class="logo-container">
          <span>DashBoard</span>
        </div>

        <el-menu default-active="2" class="el-menu-vertical-demo" background-color="#545c64"text-color="#fff"active-text-color="#ffd04b">
          <el-menu-item index="2">
            <i class="el-icon-menu"></i>
            <span>Options</span>
          </el-menu-item>
        
          <el-menu-item index="4">
            <i class="el-icon-setting"></i>
            <span>Values</span>
          </el-menu-item>
        </el-menu>
      </el-aside>
      
      <el-container>
        <el-header>
          <el-menu :default-active="activeIndex" class="el-menu-demo" mode="horizontal">
            <el-menu-item index="1">HomePage</el-menu-item>
            <el-menu-item index="3">Info</el-menu-item>
          </el-menu>
        </el-header>
        <el-main>
        <el-table
          :data="tableData"
          style="width: 100%; padding: 20px">
          <el-table-column
            prop="date"
            label="Date"
            width="180">
          </el-table-column>
          <el-table-column
            prop="name"
            label="Name"
            width="180">
          </el-table-column>
          <el-table-column
            prop="address"
            label="Address">
          </el-table-column>
        </el-table>
        <el-card class="box-card">
            <div slot="header" class="clearfix">
              <span>Card name</span>
            </div>
            <div v-for="o in 4" :key="o" class="text item">
              {{'List item ' + o }}
            </div>
        </el-card>
        </el-main>
      </el-container>
    </el-container>
  </div>
</template>

<script>
import HelloWorld from './components/HelloWorld.vue'
import 'reset-css'

export default {
  name: 'app',
  components: {
    HelloWorld
  },
  data() {
    return {
      activeIndex: '2',
      tableData: [{
            date: '2016-05-03',
            name: 'Tom',
            address: 'No. 189, Grove St, Los Angeles'
          }, {
            date: '2016-05-02',
            name: 'Tom',
            address: 'No. 189, Grove St, Los Angeles'
          }, {
            date: '2016-05-04',
            name: 'Tom',
            address: 'No. 189, Grove St, Los Angeles'
          }, {
            date: '2016-05-01',
            name: 'Tom',
            address: 'No. 189, Grove St, Los Angeles'
          }]

    }
  },
  methods: {

  }
}
</script>

<style>
#app {
  font-family: Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  color: #2c3e50;
}

.container {
  max-width: 1200px;
  margin: auto;
}

.el-aside {
  background: #545c64;
  color: white;
  min-height: 100vh;
}

.logo-container {
  padding: 22px;
  background: #434A50;
}

.el-menu {
  border-right: 0 !important;
}

.el-main {
  background: #EEF1F4;
}

.breadcrumb-container {
  margin-top: 20px;
  margin-bottom: 40px;
}

.button-container {
  margin-top: 20px;
}
.text {
    font-size: 14px;
  }

  .item {
    margin-bottom: 18px;
  }

  .clearfix:before,
  .clearfix:after {
    display: table;
    content: "";
  }
  .clearfix:after {
    clear: both
  }

  .box-card {
    width: 480px;
  }
</style>
