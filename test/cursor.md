# cursor前端实践

## 一、生成静态页面代码

**全程都要以前端平时开发的视角与步骤完成对话**

- 生成整体页面布局

  给上图片

```
生成像这张图这样的uniapp页面，使用uniapp语言实现。
整个页面优先使用uviewplus(组件以up打头),
首先你需要先分析当前页面可以由哪些uviewplus组件组成,分析当前页面由哪几个模块构成,每个模块的布局和样式应该如何设计
思考后, 最后才开始编写代码, 给出完整的代码以及对应的模拟数据
```

- 继续生成页面优化

给上图片

```
继续优化内容,样式,设计, 注重给出图片的细节设计，给出完整的代码和模拟数据
```

- 分模块处理

先交给 gpt4o分析当前模块的页面布局

给上图片	

```
你是一个优秀的前端工程师, 现在你根据图片详细说明图片中的内容的布局, 按照分为几个区域 ,每个区域的又分为几个区域, 区域的内容分别是什么, 以前端视角给出专业的布局设计回答要求:
先给出整体布局结构, 再分区域解释, 只需要给出布局设计,包括位置和内容, 不需要给出具体的前端css或者布局
```

再交给 cursor 进行代码修改 ,  内容为上一步操作的结果与截图

```
优化内容,样式,设计, 注重给出图片的细节设计
```

- 组件抽离

```
丰富和优化xxxx(模块名称)的内容,样式，UI ， 
我详细的进行说明来作为优化的要求， 
xxxx(模块名称)的每个子项封装成一个组件（放入 components下，
新增一个组件的名称包，组件的文件全部为 index.vue） 
组件区域:  (gpt4o分析当前模块的页面布局结果)
```

其他场景语句:

> 结构相关

1. **创建容器**：添加一个新的容器元素，比如 `div`，用于包裹页面中的内容或特定区域。
2. **添加父容器**：新建一个父级容器，将几个已有区域包裹在其中，形成嵌套结构。
3. **划分区域**：将页面分为多个结构区域，比如导航栏、主内容区、侧边栏、页脚等。
4. **嵌套布局**：在一个容器内再嵌套子容器，用于实现多层次的布局。
5. **增加页面模块**：在页面中新增一个功能模块，比如卡片、表单、轮播图等。
6. **添加导航栏**：在页面顶部或侧边添加一个导航栏，用于链接不同页面或页面内区域。
7. **分割线**：在两个元素之间添加分割线，以视觉上分隔内容区域。

> 布局相关

1. **栅格系统**：使用网格布局（Grid）或弹性布局（Flexbox）来实现响应式栅格系统。
2. **设置 Flexbox 布局**：应用 `display: flex`，调整子元素的对齐、间距、方向等。
3. **使用 Grid 布局**：通过 `display: grid` 创建二维布局，定义行列分布。
4. **定宽和自适应布局**：指定元素的固定宽度或自适应宽度，让页面在不同设备上呈现合理的布局。
5. **固定元素位置**：设置元素为固定位置（例如 `position: fixed`），保持它在滚动时可见。
6. **流体布局**：使用百分比宽度和视口单位，让元素在不同屏幕上自动调整大小。

> 样式相关

1. **添加边距和填充**：通过 `margin` 和 `padding` 设置元素的外间距和内间距。
2. **背景色**：为元素设置背景色，使其与其他内容区分开来。
3. **设置字体样式**：调整字体的大小、粗细、颜色和行高等。
4. **边框样式**：添加边框，调整其宽度、颜色和样式（例如实线、虚线）。
5. **圆角效果**：使用 `border-radius` 创建圆角效果，比如将按钮或卡片设置为圆角。
6. **阴影效果**：应用 `box-shadow` 或 `text-shadow` 增加立体感。
7. **过渡动画**：为元素设置 `transition`，实现平滑的样式变化效果。

> 响应式设计

1. **媒体查询**：使用媒体查询调整不同屏幕宽度下的样式和布局。
2. **断点优化**：在不同屏幕尺寸的断点处优化布局和样式，例如在移动端隐藏一些元素。
3. **自适应图片**：使用 `max-width: 100%` 使图片在小屏幕上自动缩放。
4. **响应式字体**：根据屏幕大小调整字体尺寸，让文字在不同设备上易读。

> 交互与功能

1. **悬停效果**：为元素添加 `hover` 样式，使用户悬停时显示不同的效果。
2. **点击事件**：为按钮、链接等添加点击事件触发的样式或行为。
3. **表单校验**：在表单提交前检查输入内容是否符合规则。
4. **动态显示和隐藏**：通过 `display` 或 `visibility` 控制元素的显示与隐藏状态。
5. **滚动侦听**：在页面滚动时触发事件，比如显示回到顶部按钮。
6. **动画效果**：使用 CSS 动画或 JavaScript 增强页面动态效果，比如淡入、缩放、旋转等。