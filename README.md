# react-search-table

![](react-search-table.png)

#### Todo list

- 渲染数据结构
- 数据请求（url,method）
- 操作（重置条件、时间）
- 其他
  - 换页 重置 url

#### 数据结构
```
search-table {
  // 条件区
  search:[
    {
      id:'age',
      type:'text',
    },{
      id:'name',
      placeholder:'请输入姓名',
      type:'text'
    },
    {
      id:'tel',
      label:'电话',
      placeholder:'请输入',
      type:'text'
    },{
      id:'area',
      label:'地区',
      type: 'select',
      init: 0,
      data:[
        {
          value: 0,
          text: '河南',
          checked: true,
        },{
          value: 1,
          text: '北京'
        }
      ]
    },{
      id:'startTime',
      label: '开始时间',
      type:'date'
    },{
      id:'endTime',
      label: '结束时间',
      type:'date'
    },{
      label:'搜索',
      type:'submit',
      url:'/getusername',
      method:'GET',
      data:{
        id:1
      }
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
      type:'text|select|date|button|submit|action',
      [init:0,]
      [url:'',
      method:'',
      data:{},]
      [data:[
        {
          key: 0,
          value: '项目一'
        }
      ],]
      [action:()=>{

      },]
      [onEnd:()=>{

      },]
    }
  ],
  // 附加区 - 换页触发
  onchange:(pagedata)=>{
    return '<h1>附加区</h1>'
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