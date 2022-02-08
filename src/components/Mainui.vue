<template>
  <el-container class="el-container">
    <el-aside class="el-aside">
      <p><i class="far fa-star"> Enterprise Portal</i></p>
      <el-menu class="el-menu">
        <el-submenu index="1">
          <template slot="title"
            ><span
              ><i class="Nav-icon el-icon-menu"> Dashboard</i></span
            ></template
          >
        </el-submenu>

        <el-submenu index="2">
          <template slot="title"
            ><span><i class="Nav-icon el-icon-menu"> Hosts</i></span></template
          >
          <el-menu-item-group>
            <template slot="title">Group 1</template>
            <el-menu-item index="2-1">Option 1</el-menu-item>
            <el-menu-item index="2-2">Option 2</el-menu-item>
          </el-menu-item-group>
          <el-menu-item-group title="Group 2">
            <el-menu-item index="2-3">Option 3</el-menu-item>
          </el-menu-item-group>
          <el-submenu index="2-4">
            <template slot="title">Option 4</template>
            <el-menu-item index="2-4-1">Option 4-1</el-menu-item>
          </el-submenu>
        </el-submenu>

        <el-submenu index="1">
          <template slot="title"
            ><i class="Nav-icon el-icon-menu"> Bonds</i></template
          >
        </el-submenu>

        <el-submenu index="1">
          <template slot="title"
            ><i class="Nav-icon el-icon-menu"> Spaces</i></template
          >
        </el-submenu>

        <el-submenu index="3">
          <templat slot="title">
            <i class="Nav-icon el-icon-setting"> Policies</i></templat
          >
          <el-menu-item-group>
            <template slot="title">Group 1</template>
            <el-menu-item index="3-1">Option 1</el-menu-item>
            <el-menu-item index="3-2">Option 2</el-menu-item>
          </el-menu-item-group>
          <el-menu-item-group title="Group 2">
            <el-menu-item index="3-3">Option 3</el-menu-item>
          </el-menu-item-group>
          <el-submenu index="3-4">
            <template slot="title">Option 4</template>
            <el-menu-item index="3-4-1">Option 4-1</el-menu-item>
          </el-submenu>
        </el-submenu>
      </el-menu>
    </el-aside>

    <!-- main header -->
    <el-container>
      <el-header class="header">
        <el-select v-model="value" placeholder="Select">
          <el-option
            v-for="item in options"
            :key="item.value"
            :label="item.label"
            :value="item.value"
          >
          </el-option>
        </el-select>

        <el-dropdown class="header-dropdown">
          <i class="far fa-moon"></i>
          <el-dropdown-menu slot="dropdown">
            <el-dropdown-item>View</el-dropdown-item>
            <el-dropdown-item>Add</el-dropdown-item>
            <el-dropdown-item>Delete</el-dropdown-item>
          </el-dropdown-menu>
        </el-dropdown>

        <el-dropdown class="header-dropdown">
          <i class="fas fa-code"></i>
          <el-dropdown-menu slot="dropdown">
            <el-dropdown-item>View</el-dropdown-item>
            <el-dropdown-item>Add</el-dropdown-item>
            <el-dropdown-item>Delete</el-dropdown-item>
          </el-dropdown-menu>
        </el-dropdown>

        <el-dropdown class="header-dropdown">
          <i class="el-icon-question"></i>
          <el-dropdown-menu slot="dropdown">
            <el-dropdown-item>View</el-dropdown-item>
            <el-dropdown-item>Add</el-dropdown-item>
            <el-dropdown-item>Delete</el-dropdown-item>
          </el-dropdown-menu>
        </el-dropdown>

        <el-dropdown class="header-dropdown">
          <i class="el-icon-s-tools"></i>
          <el-dropdown-menu slot="dropdown">
            <el-dropdown-item>View</el-dropdown-item>
            <el-dropdown-item>Add</el-dropdown-item>
            <el-dropdown-item>Delete</el-dropdown-item>
          </el-dropdown-menu>
        </el-dropdown>

        <el-dropdown class="header-dropdown">
          <i class="el-icon-user">Name</i>
          <el-dropdown-menu slot="dropdown">
            <el-dropdown-item>View</el-dropdown-item>
            <el-dropdown-item>Add</el-dropdown-item>
            <el-dropdown-item>Delete</el-dropdown-item>
          </el-dropdown-menu>
        </el-dropdown>
      </el-header>

      <el-main>
        <h1>All quality of service profiles</h1>
        <el-table
          :data="tableData"
          :default-sort="{ order: 'descending' }"
          stripe
        >
          <el-table-column prop="id" sortable label="Id" width="250">
          </el-table-column>

          <el-table-column prop="name" sortable label="Name" width="400">
          </el-table-column>

          <el-table-column prop="space" sortable label="Space" width="400">
          </el-table-column>

          <el-table-column prop="bond" sortable label="Bonds" width="300">
          </el-table-column>

          <el-table-column prop="class" sortable label="Classes" width="200">
          </el-table-column>
        </el-table>
      </el-main>
    </el-container>
  </el-container>
</template>

<script>
export default {
  name: "Mainui",
  data() {
    return {
      tableData: [
        {
          id: 1,
          name: "John Brown",
          space: "parentdev",
          bond: 5,
          class: 1,
        },
        {
          id: 2,
          name: "Jim Green",
          space: "parentdev",
          bond: 20,
          class: 2,
        },
        {
          id: 3,
          name: "Joe Blck",
          space: "parentdev",
          bond: 2,
          class: 1,
        },
        {
          id: 4,
          name: "nathan",
          space: "parentdev",
          bond: 2,
          class: 1,
        },
        {
          id: 4,
          name: "nathan",
          space: "parentdev",
          bond: 2,
          class: 1,
        },
        {
          id: 4,
          name: "nathan",
          space: "parentdev",
          bond: 2,
          class: 1,
        },
        {
          id: 4,
          name: "nathan",
          space: "parentdev",
          bond: 2,
          class: 1,
        },
        {
          id: 4,
          name: "nathan",
          space: "parentdev",
          bond: 2,
          class: 1,
        },
        {
          id: 4,
          name: "nathan",
          space: "parentdev",
          bond: 2,
          class: 1,
        },
        {
          id: 4,
          name: "nathan",
          space: "parentdev",
          bond: 2,
          class: 1,
        },
        {
          id: 4,
          name: "nathan",
          space: "parentdev",
          bond: 2,
          class: 1,
        },
      ],
    }
  },
}
</script>

<style scoped>
.header-dropdown {
  font-size: 20px;
  padding-top: 10px;
  padding-left: 18px;
}
.header {
  text-align: right;
  font-size: 12px;
  box-shadow: 0 4px 8px 0 rgba(0, 0, 0, 0.2);
  height: 50px;
}
.el-menu {
  background-color: #297aca;
  color: white;
}

.el-aside {
  width: 300px;
  background-color: #257ace;
  color: white;
}
.el-container {
  color: white;
  height: 900px;
  border: 1px solid #eee;
}
.Nav-icon {
  color: rgb(232, 232, 232);
}
</style>
