# react-search-table

![](react-search-table.png)

#### 数据结构
```
search-table {
  // 条件区
  search:[
    {
      type:'text',
    },{
      placeholder:'请输入姓名',
      type:'text'
    },
    {
      label:'姓名',
      placeholder:'请输入',
      type:'text'
    },{
      type: 'select',
      select:[
        {
          value: 0,
          text: '项目一'
        },{
          value: 1,
          text: '项目一'
        }
      ]
    },{
      label:'搜索',
      type:'submit'
    },{
      label:'新增',
      type:'action',
      action:()=>{
        // 弹框、跳转
      }
    },
    {
      [label:'demo',]
      [placeholder:'请输入',]
      type:'text|select|date|submit|action',
      [select:[
        {
          key: 0,
          value: '项目一'
        }
      ]],
      [action:()=>{

      }]
    }
  ],
  // 附加区 - 换页触发
  onchange:(pagedata)=>{

  },

  // 数据区
  header:['姓名','电话', '性别'],
  data:[
    {
      id: 'name',
      name: '姓名',
    },{
      id: 'tel',
      name: '电话',
      render:(val,record)=>{

      }
    },{
      id: 'age',
      name: '年龄',
      sortable: true
    }
  ]
}
```