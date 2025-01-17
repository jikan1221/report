## 简要说明

图表配置项的中文名称基本都是直接使用Echarts图表组件对应定义的名称，非Echarts图表组件则根据功能进行命名。<br>
每个图表组件的配置项都不尽相同，配置项的作用在于调整图表、数据的展示样式，这里着重说明一些共有的配置项和特殊的配置项，因为并不是按照一个图表一个配置项介绍的，没有介绍的部分请自行尝试了。

## 图层名称

**定义：** 顾名思义，定义该组件在图层中显示的名称。<br>
**使用建议：** 因为图层名称是可以重复的，所以在图层中无法准确判断该图层具体对应哪个组件，且在大屏画布中有的图表组件因为置底或者上层覆盖了别的组件，导致很难选到这个图表，如果修改了图层名称，则可以通过图层快速定位并选中该组件。

## 文本框--文本内容

文本框和滚动文本这两个组件，修改数据--静态数据，是不会生效的，文本内容配置项中写的内容才是真正的静态数据。<br>

## 超链接--跳转方式

**使用建议：** 默认的跳转方式是本窗口，实际使用还是请选择新窗口。<br>

## 图片地址

**定义：** 图片对应的url链接 <br>
**使用建议：**
这里图片的url因为只要是链接能打开就行了，所以适用性范围很广，但一般考虑到网络传输、安全性等问题，建议自行上传图片，然后用系统生成的链接地址；注意目前系统赞不支持svg图片，因此图片可能存在畸变，要注意缩放比例。

## 表格--滚动间隔

**定义：** 表格数据滚动的间隔，受到"开启滚动"、"动效时间"、"滚动个数"、"数据--动态数据--刷新时间"影响 <br>
**使用建议：**
表格动态数据默认是5s请求一次数据，因此每隔5s图表就会刷新一次，这时就会重置滚动时间，会出现滚动到某个值时回到开头重新滚动。想让表格把每个值都滚动显示到的话，可以减少滚动间隔时间，去掉动效时间，增大滚动个数，提高动态数据刷新时间。<br>

## 柱体设置

**定义：** 修改柱体的形状等，涉及柱状图、柱线图 <br>
**使用建议：** 当数据条目数很少时，比如默认的静态数据是5条，放大宽度，柱体变得更粗，搭配"竖展示"
配置项，可以得到更好的展示效果；当只有一个值的时候，通过XY不展示，可以得到单独的一根柱子。<br>

## 折线设置

**定义：** 修改点/折线的展示效果，涉及折线图、柱线图 <br>
**使用建议：** 当折线的量少的时候，可以选择拉大"面积厚度"，折线多了，就会相关覆盖，效果反而不好。<br>

## 标题设置

**定义：** 给图表组件添加标题/表头/title。 <br>
**使用建议：**
一般没有图例功能的图表组件可以直接使用这个功能，因为可能会和图例重叠。有图例的图表组件要定义图表的话，可用文本框拖动到图表上方，作为标题。<br>

## X轴设置

**定义：** 定义坐标轴中的X轴的相关设置项。 <br>
**使用建议：**
可以修改坐标轴的颜色，因为默认是纯白色，所以部分浏览器可能显示不出来；可以设置坐标名（柱状对比图不存在此配置项）；如果数值相对密集的话，可以调整"
数值间隔"。

## Y轴设置

**定义：** 定义坐标轴中的Y轴的相关设置项。 <br>
**使用建议：** 可以修改坐标轴的颜色，因为默认是纯白色，所以部分浏览器可能显示不出来；如果数值相对密集的话，可以调整"均分"
；注意"缩放"配置项只会对那些数据差距较大时才会生效。

## 图例操作

**定义：** 图例的直接来源是数据中的数值，比如在堆叠图中，图例的值就是"动态数据-Y轴字段"
字典选择的字段数值，可以简单的认为是“数据分类”。<br>
**使用建议：** 填写图例名称，修改图例的值，使用"|"进行分隔，相当于别名。<br>

## 数值设定

**定义：** 设定数据在图表中的显示配置。<br>
**使用建议：** 对于堆叠图、柱线图等等柱体、折线多的，不建议显示。<br>

## 提示语设置

**定义：** 设定提示，主要用于当鼠标选中/滑动时，显示数据对应的值。<br>
**使用建议：**
设定和对应图表相反的颜色，鼠标滑动时则会醒目；注意此配置项必须保存预览鼠标选中后才能看到效果，在画布设计是看不到效果的。<br>

## 自定义配色

**使用建议：** 如果不设置的话，默认就是大红色；默认按顺序给数值赋予颜色。<br>

## 饼图样式/模式

**定义：** 定义饼图显示的样式、模式，涉及饼图、南丁格尔玫瑰图。<br>
**使用建议：** 按数据量多少进行选择样式。<br>

