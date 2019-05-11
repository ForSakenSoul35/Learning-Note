# ListView 
## dateSource
ListView需要指定数据的来源，传入数据必须是数组，或者字典里面包括数组。
原始数据可以是简单的字符串数组，也可以是复杂嵌套的对象-分不同去 各自包含若干行数据

不同的是，无法向原生一样去显示指定section和row的个数，系统会根据你传入的数据自动生成section和row
官方希望我们在构造函数中指定ListView 的取值策略。在使用dataSource时，需要先new一个dataSource对象

更新dataSource中的数据，每次都重新调用cloneWithRows方法（如果用到了section，则对应cloneWithRowsAndSections方法）
数据源中的数据本身是不可修改的，clone方法会自动提取新数据并进行逐行对比，使用rowHasChanged的策略

```
const ds = new ListView.DataSource({
  rowHasChanged:(row1,row2)=>true
})
```
- 参数
接受4个参数 都是可选的
  * getRowData(dataBlob,sectionID,rowID):表明我们将以何种方式dataBlob中提取出rowData,sectionID用于指定每一个section的标题名（在renderRow,renderHeader等方法中会默认拆开）
