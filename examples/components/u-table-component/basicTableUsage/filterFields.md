```html
<template>
<div>
  <el-button @click="openDialog">点我可以打开筛选字段弹窗</el-button>
  <u-table
    style="margin-top: 20px;"
    ref="plTable"
    :data="tableData"
    moveDownIcon="el-icon-caret-bottom"
    moveUpIcon="el-icon-caret-top"
    :showDialogIcon="true"
    height=500
    field-title="u-table选择显示字段"
    :field-sort="true"
    :dialog-data="dialogData"
    border>
    <u-table-column
      fixed
      prop="date"
      label="日期"
      width="150">
    </u-table-column>
    <u-table-column
      prop="name"
      label="姓名"
      width="120">
    </u-table-column>
    <u-table-column
      prop="province"
      label="省份"
      width="120">
    </u-table-column>
    <u-table-column
      prop="city"
      label="市区"
      width="120">
    </u-table-column>
    <u-table-column
      prop="address"
      label="地址"
      width="300">
    </u-table-column>
    <u-table-column
      prop="zip"
      label="邮编"
      width="120">
    </u-table-column>
    <u-table-column
      fixed="right"
      label="操作"
      width="160">
      <template slot="header" slot-scope="scope">
          <div>操作<span style="margin-left: 10px;color:red" @click="openDialog">点我试试看</span></div>
     </template>
      <template slot-scope="scope">
        <el-button @click="handleClick(scope.row)" type="text" size="small">查看</el-button>
        <el-button type="text" size="small">编辑</el-button>
      </template>
    </u-table-column>
  </u-table>
</div>
</template>

<script>
  export default {
    methods: {
      handleClick(row) {
        console.log(row);
      },
      openDialog () {
        this.$refs.plTable.plDialogOpens()
      }
    },

    data() {
      return {
        // dialogData跟你的列数， 最好自己保持一致吧，这个随便你保持一致还是不保持一致
        dialogData: [
          // { name: '我的', // 字段名 state: true, // 选择状态 disabled: true // 是否禁用 }]
          { name: '日期',  state: true, disabled: true },
          { name: '姓名', disabled: true },
          { name: '省份' },
          { name: '地址' },
          { name: '邮编' },
        ],
        tableData: [{
          date: '2016-05-02',
          name: '王小虎',
          province: '上海',
          city: '普陀区',
          address: '上海市普陀区金沙江路 1518 弄',
          zip: 200333
        }, {
          date: '2016-05-04',
          name: '王小虎',
          province: '上海',
          city: '普陀区',
          address: '上海市普陀区金沙江路 1517 弄',
          zip: 200333
        }, {
          date: '2016-05-01',
          name: '王小虎',
          province: '上海',
          city: '普陀区',
          address: '上海市普陀区金沙江路 1519 弄',
          zip: 200333
        }, {
          date: '2016-05-03',
          name: '王小虎',
          province: '上海',
          city: '普陀区',
          address: '上海市普陀区金沙江路 1516 弄',
          zip: 200333
        },
        {
          date: '2016-05-02',
          name: '王小虎',
          province: '上海',
          city: '普陀区',
          address: '上海市普陀区金沙江路 1518 弄',
          zip: 200333
        }, {
          date: '2016-05-04',
          name: '王小虎',
          province: '上海',
          city: '普陀区',
          address: '上海市普陀区金沙江路 1517 弄',
          zip: 200333
        }, {
          date: '2016-05-01',
          name: '王小虎',
          province: '上海',
          city: '普陀区',
          address: '上海市普陀区金沙江路 1519 弄',
          zip: 200333
        }, {
          date: '2016-05-03',
          name: '王小虎',
          province: '上海',
          city: '普陀区',
          address: '上海市普陀区金沙江路 1516 弄',
          zip: 200333
        },
         {
          date: '2016-05-02',
          name: '王小虎',
          province: '上海',
          city: '普陀区',
          address: '上海市普陀区金沙江路 1518 弄',
          zip: 200333
        }, {
          date: '2016-05-04',
          name: '王小虎',
          province: '上海',
          city: '普陀区',
          address: '上海市普陀区金沙江路 1517 弄',
          zip: 200333
        }, {
          date: '2016-05-01',
          name: '王小虎',
          province: '上海',
          city: '普陀区',
          address: '上海市普陀区金沙江路 1519 弄',
          zip: 200333
        }, {
          date: '2016-05-03',
          name: '王小虎',
          province: '上海',
          city: '普陀区',
          address: '上海市普陀区金沙江路 1516 弄',
          zip: 200333
        }]
      }
    }
  }
</script>
```

