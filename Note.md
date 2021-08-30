# 技术栈
1. 基于flexible.js（用来适配移动端的javascript框架） + rem 智能大屏适配
2. VScode cssrem插件
3. Flex布局
4. Less使用
5. 基于ECharts数据可视化展示
6. ECharts柱状图数据设置
7. ECharts地图引入

# 适配方案
1. flexible.js把屏幕分为24等份 每一等份是80px
2. cssrem插件的基准值是80px（插件-配置按钮-配置扩展设置-root font size里面设置） 

# ECharts介绍
常见的数据可视化库：
1. D3.js 目前Web端评价最高的JS可视化工具库
2. ECharts.js 百度出品的开源JS数据可视化库
3. Highcharts.js 国外的前端数据可视化库
4. AntV 蚂蚁金服全新一代数据可视化解决方案

是一个JS插件，性能好可流畅运行PC与移动设备，兼容主流浏览器，提供更多常用图表，且可定制。


# ECharts五部曲
1. 下载并引入echarts.js文件
2. 准备一个具备大小的DOM容器（生成图表放入这个容器内）
3. 初始化echarts实例对象  
   var myChart = echarts.init(document.querySelector(".box"))
4. 指定配置项和数据（根据具体需求修改配置选项） option
5. 将配置项设置给echarts实例对象（让echarts对象根据修改好的配置生效）
   myChart.setOption(option)

# ECharts基础配置option
color(设置线条颜色，数组)
title
tooltip(提示框组件, trigger: axis/item)
legend(图例)
toolbox(工具箱, 可以另存图片等功能)
xAxis(value/category/log, boundaryGap:是否让线条和坐标轴有缝隙), yAxis
{
    axisTick: 刻度线
    axisLine: 坐标轴
    axisLabel: 坐标刻度文字
    splitLine: 分割线
}
grid(控制图表大小, 距离DOM容器的距离, containLabel true显示刻度标签)series(决定显示图表类型, series里有name legend可以删掉)
{
    barCategoryGap: 柱子之间的距离
    barWidth: 柱子的宽度
    yAxisIndex: 层级
    itemStyle: 柱子更改样式
    label: 显示柱子内的文字
}
{
    smooth: 光滑曲线
    areaStyle: 填充颜色
    symbol, symbolSize, itemStyle: 拐点设置
}

# 立即执行函数
为了防止变量污染，减少命名冲突，里面的变量是局部变量。

