<template>
  <div>
    <!--    <hello></hello>-->
    <el-data-table v-bind="tableConfig"></el-data-table>
  </div>
</template>

<script>
export default {
  // components: {
  //   hello,
  // },
  data() {
    return {
      tableConfig: {
        url: '/example/users',
        columns: [
          {
            prop: 'componentName',
            label: '组件名称'
          },
          {
            prop: 'fflz',
            label: '分类'
          },
          {
            prop: 'version',
            label: '版本'
          },
          {
            prop: 'lang',
            label: '开发语言'
          },
          {
            prop: 'time',
            label: '最后更新时间'
          },
          {
            prop: 'state',
            label: '状态'
          }
        ],
        searchForm: [
          {
            $type: 'input',
            $id: 'name',
            label: '组件名称',
            $el: {
              placeholder: '请输入'
            }
          },
          {
            $type: 'select',
            $options: [{label: '测试', value: 'test'}],
            $id: 'item',
            label: '分类',
            $el: {
              placeholder: '请选择'
            }
          },
          {
            $type: 'select',
            $options: [{label: '测试', value: 'test'}],
            $id: 'state',
            label: '状态',
            $el: {
              placeholder: '请选择'
            }
          }
        ],
        form: [
          {
            $type: 'input',
            $id: 'componentName',
            label: '组件名称',
            $el: {
              placeholder: '请输入'
            },
            rules: [
              {
                required: true,
                message: '请输入用户名',
                trigger: 'blur'
              }
            ]
          }
        ]
      }
    }
  }
}
</script>
